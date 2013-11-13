Yasobjc is a tool for yasnippet snippet generation for objective-c
library (cocoa/iphone SDK).

Basic Usage: `yasobjc.rb -o DIR file1 file2 ...`

`-o DIR`: The output directory for the snippets generated

Example:

    find /Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS4.0.sdk/System/Library/Frameworks -name "*.h" | xargs yasobjc.rb -o ~/.emacs.d/yasnippet/objc-mode

or in XCode 5:

    find /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS7.0.sdk/System/Library/Frameworks -name "*.h" | xargs ./yasobjc.rb -o ~/.emacs.d/yasnippet/objc-mode

which will generate all snippets into standard yasnippet directory.

One snippet is generated per objective-c function, and the snippets
are categoried by header file name. For example, all functions
`NSString.h` will be in `NSString` category.

It's recommended to use ETAGS plus auto-complete library for better
completion experience.
