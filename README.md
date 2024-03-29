# *swipe4u* &middot;       [![](https://img.shields.io/badge/code%20style-c%23%20standard-brightgreen.svg?style=flat)](<https://github.com/raywenderlich/c-sharp-style-guide>) ![](https://img.shields.io/badge/dev%20status-30%25-orange.svg?style=flat)
Swipe4u is a library that helps you using swipes in the Unity development. You don't have to struggle developing the logic behind them anymore

## Features
Swipe4u provides ready made scripts for all kind of swipes. There is also a factory that helps you choosing the detector that fits you the best. Check it out with a little example down below

In the next commits, common touch handling patterns will be implemented. 

## How to use it

Use it inside the update() function of a Unity script:

```c#
public SwipeDetector detector = new CoolSwipeDetector();
public OnSwipe action = delegate { /*action triggered by swipe*/};

void Update()
{
	Touch[] touches = Input.Touches;
    
	detector.DetectSwipe(ref touches, SwipeDirection.Right, action, minSwipeDistance);
}		

```

If you don't know which detector to use:

```c#
SwipeSetting[] settings = new SwipeSetting[] {SwipeSetting.WHEN_TOUCH_END, ...};
SwipeDetectorFactory factory = new SwipeDetectorFactory(settings);

SwipeDetector detector = factory.GetSwipeDetector();
```

## Framework used

<b>Built with</b>

- Visual Studio 2017

**Tested with**

- Unity

## Contribute

Contributors are welcome! Feel free to fork, pull request, open issues or propose new features

## License
Mozilla Public License 2.0
