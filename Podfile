platform :ios, '13.0'

use_frameworks!
inhibit_all_warnings!

target 'BaseStore' do
  inherit! :search_paths

  pod 'SwiftLint'

  target 'BaseStoreTests' do
    pod "Cuckoo"
    pod 'SwiftHamcrest'
  end
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings.delete 'IPHONEOS_DEPLOYMENT_TARGET'
    end
  end
end
