Intro
==============
kim's code

Animated Social share buttons control.<br>
Supported share buttons:<br><b>Facebook</b>,  <b>Twitter</b>,  <b>Google+</b>, <b>Tumblr</b>, <b>Vkontakte (vk.com)</b>, <b>LinkedIn</b>, <b>Pinterest</b>, <b>Youtube</b>, <b>Vimeo</b>, <b>Reddit</b>, <b>E-mail</b>

<img src="http://mixdesign.kz/external/AAShareBubblesAbay.png?tmp"/>&nbsp;&nbsp;
<img src="http://mixdesign.kz/external/AAShareBubbles.png?6"/>

Installation
------

Two ways:<br>
1. Just drag n drop **AAShareBubbles** folder into your xcode project.<br>
2. **Cocoapods:**
```ruby
pod 'AAShareBubbles'
```
Usage:
------
```objective-c
#import "AAShareBubbles.h"
```
```objective-c
AAShareBubbles *shareBubbles = [[AAShareBubbles alloc] initWithPoint:CGPointMake(100, 100)
                                                              radius:100
                                                              inView:self.view];
shareBubbles.delegate = self;
shareBubbles.bubbleRadius = 45; // Default is 40
shareBubbles.showFacebookBubble = YES;
shareBubbles.showTwitterBubble = YES;
shareBubbles.showMailBubble = YES;
shareBubbles.showGooglePlusBubble = YES;
shareBubbles.showTumblrBubble = YES;
shareBubbles.showVkBubble = YES;
[shareBubbles show];
````
#####Delegate
```objective-c
-(void)aaShareBubbles:(AAShareBubbles *)shareBubbles tappedBubbleWithType:(AAShareBubbleType)bubbleType
{
    switch (bubbleType) {
        case AAShareBubbleTypeFacebook:
            NSLog(@"Facebook");
            break;
        case AAShareBubbleTypeTwitter:
            NSLog(@"Twitter");
            break;
        case AAShareBubbleTypeMail:
            NSLog(@"Email");
            break;
        case AAShareBubbleTypeGooglePlus:
            NSLog(@"Google+");
            break;
        case AAShareBubbleTypeTumblr:
            NSLog(@"Tumblr");
            break;
        case AAShareBubbleTypeVk:
            NSLog(@"Vkontakte (vk.com)");
            break;
        default:
            break;
    }
}

-(void)aaShareBubblesDidHide {
    NSLog(@"All Bubbles hidden");
}

```

Requirements:
------------
`ARC`, `iOS 5+`, `Xcode 4+`

Todo:
-------
- Add more social buttons.
- Add opportunity to show bubbles in specified order.
