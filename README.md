FontAwesome-iOS
===================

Brings the iconic FontAwesome font to iOS.

Installation
--------------------

Add this to your `Podfile`:

```
pod 'FontAwesome'
```

This will include the helper files, and the font resource automatically in your app.

Usage
--------------------

First, make sure you have `FontAwesome.ttf` bundled in your project and that `UIAppFonts` key in the project's plist file contains a String item named `FontAwesome.ttf`.

Then add the `NSString+FontAwesome` category to the project.

```
UILabel *label = [...]
label.font = [UIFont fontWithName:kFontAwesomeFamilyName size:20];
```

You can now use enums for all the different iconic characters

```
label.text = [NSString fontAwesomeIconStringForEnum:FAGithub];
```

 or you can reference them by using the class identifiers listed here http://fortawesome.github.com/Font-Awesome/#all-icons

```	
label.text = [NSString fontAwesomeIconStringForIconIdentifier:@"fa-github"];
```

That's it! For further information have a look to the small demo project!

Placeholder Image
--------------------

FAImageView is now extended and contains a new property called `defaultView` that is shown when the image is set to nil.

It is possible to use one the font-awesome icon as a default placeholder for an image view.

```
FAImageView *imageView = [[FAImageView alloc] initWithFrame:CGRectMake(0.f, 0.f, 100.f, 100.f)];
imageView.image = nil;
[imageView setDefaultIconIdentifier:@"fa-github"];
```

License
-------------------

(forked from https://github.com/alexdrone/ios-fontawesome, to be available as a CocoaPod)

Attribution is no longer required as of Font Awesome 3.0 but is much appreciated: "Font Awesome by Dave Gandy - http://fontawesome.io".

