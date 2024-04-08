#Comment the next line if you don't want to use dynamic frameworks
use_frameworks!

workspace 'LoginRadiusSwiftSDK'

platform :ios, '11.0'


target 'SwiftDemo' do
    project 'Example/SwiftDemo/SwiftDemo.xcodeproj'
    pod 'LoginRadiusSwiftSDK', :path => './'
    pod 'Eureka'
    pod 'SwiftyJSON', '<= 4.0'
    pod 'Alamofire', '<= 4.8.2'
    #pod 'Google/SignIn', '<= 4.1.0'
    #pod 'TwitterKit', '<= 3.4.2'
    
    post_install do |installer|
    myTargets = ['Eureka']

    installer.pods_project.targets.each do |target|
        if myTargets.include? target.name
            target.build_configurations.each do |config|
                config.build_settings['SWIFT_VERSION'] = '5.0'
            end
        end
    end
end

end
