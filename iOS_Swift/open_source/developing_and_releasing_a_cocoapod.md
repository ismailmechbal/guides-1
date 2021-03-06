# Developing and releasing a CocoaPod
Developing a CocoaPod is really easy!

## Set up
First, you'lle need to run the following command on the Terminal:

```
$ pod lib create yourPodName
```
After this, just select the options you want to work with:

* Objective-C or Swift?
* Demo application? [YES!]
* Testing framework
* View based testing

Once the scaffolding is done, you can open your project in Xcode and - almost - start coding!

## Metadata
There are three pieces to consider: 

1. **.podspec**: This files describes information about your pod and the current version.
2. **README**: The README is written in [Markdown](https://en.wikipedia.org/wiki/Markdown). The README is for other developers to understand how your project works.
3. **License**: The ```pod lib create``` command created your project with a [MIT License](https://en.wikipedia.org/wiki/MIT_License). 


## Getting the .podspec into shape
First you need to open the *.podspec* file in Xcode. You’ll find it under yourPodName/Podspec Metadata/yourPodName.podspec

Go to your terminal and run the following command:

```
$ pod lib lint yourPodName.podspec
```
This is a handy tool that let's you know what you need to fix in your file. So go ahead an do it. 

## Git
You'll need a repository to 'host' your project. Create it and commit/push your pod shell. 

## Coding
Code something awesome and useful that you think other developers would like to use. 

But before you start coding you'll need to delete this file: **ReplaceMe.swift** (Pods/Development Pods/yourPodName/Pod/Classes/). Next create a yourPodName.swift file and happy coding!

### Example project
Your example project will be under: **yourPodNAme/Example for yourPodName/ViewController.swift**. Here you can make an example of how to use your pod, this will help other developers to understand easier how it works.

**Remember to do a *pod install* in your example project.**

## Release
1. Tag your commit and push it to your repository

	```
	$ git tag 0.1.0
	$ git push origin 0.1.0
	```
2. Validate that everything is alright 

	```
	$ pod lib lint yourPodName.podspec
	```
3. Push to the CocoaPods trunk

	```
	$ pod trunk push yourPodName.podspec
	```

## Cocoa Controls
One option to give more exposure to your pod is to publish it in Cocoa Controls. This is a page where many developers share their work to make it known in the community.

[Go and check it out!](https://www.cocoacontrols.com)
