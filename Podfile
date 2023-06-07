platform :ios, '12.0'




target 'NS-3.1' do

  use_frameworks!


pod 'Firebase/Core'
pod 'Firebase/Messaging'
pod 'Firebase/Auth'
pod 'GoogleSignIn'
pod 'FBSDKLoginKit'
pod 'Alamofire', '~> 5.0.0'
pod 'Kingfisher'
pod 'SwiftIcons'
pod 'SVProgressHUD'
pod 'Cosmos'
pod "AssistantKit"
pod 'SwiftEventBus', :tag => '2.2.0', :git => 'https://github.com/cesarferreira/SwiftEventBus.git'
pod 'SwiftyJSON'
pod 'BadgeSwift'
pod 'GoogleMaps'
pod 'GooglePlaces'
pod "MXParallaxHeader"
pod "Atributika"
pod 'SkyFloatingLabelTextField'
pod 'ImageSlideshow'
pod "ImageSlideshow/Kingfisher"
pod 'Google-Mobile-Ads-SDK'
pod 'RealmSwift'
pod 'SwiftWebVC'
pod 'Fabric'
pod 'Crashlytics'
pod "SkeletonView"
pod 'libPhoneNumber-iOS'
pod 'StepIndicator'
pod "YoutubePlayer-in-WKWebView"
pod 'MercariQRScanner'



post_install do |installer|
  
  
    installer.pods_project.targets.each do |target|
          target.build_configurations.each do |config|
              config.build_settings['ONLY_ACTIVE_ARCH'] = 'NO'
              config.build_settings['BUILD_LIBRARY_FOR_DISTRIBUTION'] = 'YES'
          end
      end
	
    installer.pods_project.build_configurations.each do |config|
        config.build_settings.delete('CODE_SIGNING_ALLOWED')
        config.build_settings.delete('CODE_SIGNING_REQUIRED')
        config.build_settings["EXCLUDED_ARCHS[sdk=iphonesimulator*]"] = "arm64"
    end

    installer.pods_project.targets.each do |target|
         target.build_configurations.each do |config|
            if config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'].to_f < 9.0
              config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '9.0'
            end
         end
     end

     installer.pods_project.targets.each do |target|

	 target.build_configurations.each do |config|
             config.build_settings['SWIFT_VERSION'] = '4.0'
         end

       	if target.name == 'StepIndicator'
            target.build_configurations.each do |config|
               config.build_settings['SWIFT_VERSION'] = '5.0'
             end
        end

        if target.name == 'SkeletonView'
            target.build_configurations.each do |config|
               config.build_settings['SWIFT_VERSION'] = '5.0'
             end
        end
        
        if target.name == 'Cosmos'
            target.build_configurations.each do |config|
               config.build_settings['SWIFT_VERSION'] = '5.0'
             end
        end
        
        if target.name == 'Kingfisher'
            target.build_configurations.each do |config|
               config.build_settings['SWIFT_VERSION'] = '5.0'
             end
        end
        
        if target.name == 'BadgeSwift'
            target.build_configurations.each do |config|
               config.build_settings['SWIFT_VERSION'] = '5.0'
             end
        end
        
        if target.name == 'ImageSlideshow'
            target.build_configurations.each do |config|
               config.build_settings['SWIFT_VERSION'] = '5.0'
             end
        end

      end

end



end
