# PhotoPicker
A image picker for iOS , written by Swift.

refer: [teambition/PhotoPicker](https://github.com/teambition/PhotoPicker)

## How To Get Started
###Carthage
Specify "PhotoPicker" in your Cartfile:

```
github "StormXX/PhotoPicker"
```

## Usage
### configuration  properties
```
//MARK: - public property
open weak var delegate: PhotoPickerDelegate?
open var assetCollectionSubtypes: [PHAssetCollectionSubtype]?
open var allowMultipleSelection: Bool = true
open var minimumNumberOfSelection: Int = 1
open var maximumNumberOfSelection: Int = 9
open var mediaType: PhotoPickerMediaType = .any
open var prompt: String?

```

###  Implement delegate
```
func photoPickerController(controller: PhotoPickerController, didFinishPickingAssets assets: [PHAsset], needHighQualityImage: Bool)
func photoPickerControllerDidCancel(controller: PhotoPickerController)
func photoPickerController(controller: PhotoPickerController, shouldSelectAsset asset: PHAsset) -> Bool
func photoPickerController(controller: PhotoPickerController, didSelectAsset asset: PHAsset)
func photoPickerController(controller: PhotoPickerController, didDeselectAsset asset: PHAsset)
```

### Present PhotoPicker
```
let photoPickerController = PhotoPickerController()
photoPickerController.delegate = self
presentViewController(photoPickerController, animated: true, completion: nil)
```

## Localization
```
let localizedString: [String: String] = [
    "PhotoPicker.Cancel": LocalizationString("PhotoPicker.Cancel"),
    "PhotoPicker.OK": LocalizationString("PhotoPicker.OK"),
    "PhotoPicker.Send": LocalizationString("PhotoPicker.Send"),
    "PhotoPicker.Origin": LocalizationString("PhotoPicker.Origin"),
    "PhotoPicker.MaximumNumberOfSelection.Alert": LocalizationString("PhotoPicker.MaximumNumberOfSelection.Alert"),
    "PhotoPicker.Photos": LocalizationString("PhotoPicker.Photos"),
    "PhotoPicker.Videos": LocalizationString("PhotoPicker.Videos"),
    "PhotoPicker.Title" : LocalizationString("PhotoPicker.Title"),
    "PhotoPicker.VideoSelect.Alert": LocalizationString("PhotoPicker.VideoSelect.Alert")
        ]
```

## Similar
- [QBImagePicker](https://github.com/questbeat/QBImagePicker)(This framework is written by Objective-C)
- [Example app using Photos Framework](https://developer.apple.com/library/ios/samplecode/UsingPhotosFramework/Introduction/Intro.html)(Apple PhotoKit Sample Code)

## Minimum Requirement
- iOS 8.0

## Release Notes
- [Release Notes](https://github.com/StormXX/PhotoPicker/releases)

## License
- PhotoPicker is released under the MIT license. See [LICENSE](https://github.com/StormXX/PhotoPicker/blob/master/LICENSE) for details.

## More Info
- Have a question? Please [open an issue](https://github.com/StormXX/PhotoPicker/issues/new)!

