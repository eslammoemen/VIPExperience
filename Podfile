
platform :ios, '15.0'

source 'https://github.com/CocoaPods/Specs.git'
 
workspace 'VIPexperience.xcworkspace'
project 'VIPexperience.xcodeproj'

use_frameworks!

def _resource
  pod 'R.swift','~> 5.1.0'
  end


def _corePackage
  pod 'KRProgressHUD'
  pod 'NotificationBannerSwift'
  pod 'lottie-ios', '~> 3.0'
  pod "KRProgressHUD" , '~> 3.4.3'
  pod 'NotificationBannerSwift'
  pod 'StatusProvider'
  pod 'Kingfisher' , '~> 5.0'
  end


#================

target 'VIPexperience' do
  # Comment the next line if you don't want to use dynamic frameworks
  _resource
  _corePackage
  pod 'CropViewController'
  pod 'Alamofire'
  pod 'KDCircularProgress'
  pod 'SnapKit'
  pod 'DropDown'
  end

#================
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
	if target.name == 'R.swift.Library' ||
	   target.name == 'NotificationBannerSwift' ||
           target.name == 'CropViewController'
       	   config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '11.0'
      	end
        
    end
  end
end


target 'DNDCorePackage' do
  project 'DNDCorePackage/DNDCorePackage.project'
  _corePackage
  
  end

target 'DNDResources' do
  # Comment the next line if you don't want to use dynamic frameworks
  project 'DNDResources/DNDResources.project'
  _resource
  # Pods for iOSTest
  
  end
target 'PhotoLibraryMedia' do
  # Comment the next line if you don't want to use dynamic frameworks
  project 'PhotoLibraryMedia/PhotoLibraryMedia.project'
  pod 'CropViewController'
  _resource
  _corePackage
  # Pods for iOSTest
  
end
target 'NetworkLayer' do
  # Comment the next line if you don't want to use dynamic frameworks
  project 'NetworkLayer/NetworkLayer.project'
  # Pods for iOSTest
  _corePackage
  pod 'Alamofire'
end

target 'VIPModule' do
  # Comment the next line if you don't want to use dynamic frameworks
  project 'VIPModule/VIPModule.project'
  pod 'DropDown'
  # Pods for iOSTest
  _resource
  _corePackage
  pod 'KDCircularProgress'
  pod 'SnapKit'
  
end

