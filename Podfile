# Uncomment the next line to define a global platform for your project
platform :ios, '9.0'

target 'Swipict' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  # Pods for Swipict
  pod 'ZLSwipeableViewSwift', :git => 'https://github.com/zhxnlai/ZLSwipeableViewSwift.git', :commit => '18d6109'

end

swift4_names = [
  'ZLSwipeableViewSwift'
]

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            if swift4_names.include? target.name
                config.build_settings['SWIFT_VERSION'] = "4.0"
            else
                config.build_settings['SWIFT_VERSION'] = "4.2"
            end
        end
    end
end
