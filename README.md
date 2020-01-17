# Virgils CocoaPods Specs

This repository is for [CocoaPods](https://cocoapods.org) podspecs that are intended for public distribution, but may not necessarily be suitable or ready for CocoaPods `trunk`.

## Using this repo in an Xcode project

1. Add this pod spec repo as a source in your `Podfile`:
   ```
   source 'https://github.com/virgilius-santos/public-pod-specs.git'
   source 'https://github.com/CocoaPods/Specs.git'
   ```
   (Also add the main CocoaPods trunk repo to keep being able to install other pods.)
1. In your `Podfile`, bump the pod you want to use to a version that exists in this repo.
1. `pod install --repo-update`

## Pushing to this repo

1. `pod repo add virgils-public https://github.com/virgilius-santos/public-pod-specs` (first time only)
1. Make sure your `podspec` file has the name and version you expect. If you're mirroring a publicly available podspec (i.e., one on CocoaPods trunk) and you intend to push an alternate build, use a unique version string (e.g., `5.2.0-custom.1`).
1. `pod repo push virgils-public <framework-name-here>.podspec`
