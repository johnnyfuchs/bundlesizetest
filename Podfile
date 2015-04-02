platform :ios, '7.0'
inhibit_all_warnings!
xcodeproj 'sizetest'
source 'https://github.com/CocoaPods/Specs.git'

# debug
pod 'AFHTTPRequestOperationLogger', '~> 1.0.0'
pod 'JRSwizzle', '~> 1.0'

pod 'RestKit', '~> 0.22.0'
pod 'AFOAuth2Client', :git => 'https://github.com/jesseditson/AFOAuth2Client.git', :branch => 'working'
pod 'AFOAuth1Client', '~> 0.3.3'
pod 'LVTwitterOAuthClient', '~> 0.0.1'
pod 'Facebook-iOS-SDK', '~> 3.21.1'
pod 'googleplus-ios-sdk', '~> 1.7.1'
pod 'SDWebImage', :git => 'git@github.com:rs/SDWebImage.git', :branch => 'master'
pod 'SDWebImage/WebP', :git => 'git@github.com:rs/SDWebImage.git', :branch => 'master'
pod 'AQSWhatsAppActivity', :git => 'git@github.com:weheartit/AQSWhatsAppActivity.git', :branch => 'master'
pod 'TTTAttributedLabel', '~> 1.9.5'
pod 'MBProgressHUD', :git => 'git@github.com:jdg/MBProgressHUD.git', :branch => 'master' # need latest and cocoapods hasn't indexed it yet
pod 'CRToast', '~> 0.0.7'
pod 'FormatterKit', '~> 1.8.0'
pod 'pop'

# Video
#pod 'YTVimeoExtractor', '~> 0.0.6'
pod 'HCYoutubeParser', '~> 0.0.2'

# Analytics
pod 'FlurrySDK', '~> 4.3.0'
pod 'GoogleAnalytics-iOS-SDK', '~> 3.10'

# Ads
pod 'OpenXMSDK', '2.5.0.r1'

# Sharing
# Uncomment this once this pull is complete: https://github.com/honkmaster/TTOpenInAppActivity/pull/21
# pod 'TTOpenInAppActivity', '~> 1.0'
pod 'TTOpenInAppActivity', :git => 'https://github.com/jesseditson/TTOpenInAppActivity.git', :branch => 'ios_8_image_sharing'
pod 'uservoice-iphone-sdk', '~> 3.0'
pod "Branch"
pod 'Tapstream', '~> 2.8'

#target 'WeHeartItTests', :exclusive => true do
#  pod 'Specta', '~> 0.3'
#  pod 'Mocktail', :git => 'https://github.com/jesseditson/objc-mocktail.git', :branch => 'merged-pulls'
#  pod 'OCMock'
#  pod 'OHHTTPStubs', '~> 3.1.6'
#  target 'WeHeartIt Acceptance Tests' do
#    pod 'KIF', '~> 3.1.2'
#    pod 'googleplus-ios-sdk', '~> 1.7.1'
#  end
#end

# KIF is not working in Xcode 6
# Adding this post_install command is the solution reccomended on the KIF issue tracker
# https://github.com/kif-framework/KIF/issues/419
#
post_install do |installer|
  installer.project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['FRAMEWORK_SEARCH_PATHS'] = [ '$(PLATFORM_DIR)/Developer/Library/Frameworks' ]
    end
  end
end

