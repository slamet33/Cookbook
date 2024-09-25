# Uncomment the next line to define a global platform for your project
platform :ios, '12.0'

workspace 'Cookbook.xcworkspace'
project 'Cookbook.xcodeproj'

def common_pod
  pod 'CommonUI', :path => 'Modules/CommonUI'
end

def resources_pod
  pod 'Resource', :path => 'Modules/Resource'
end

def development_pods
  common_pod
  resources_pod
end

target 'Cookbook' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!
  
  development_pods
  
  pod 'SwiftLint'
end

target 'CommonUI' do
  use_frameworks!
  project 'Modules/CommonUI/Example/CommonUI.xcodeproj'
  
  common_pod
end

target 'Resource' do
  use_frameworks!
  project 'Modules/Resource/Example/Resource.xcodeproj'
  
  resources_pod
end
