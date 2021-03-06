# KVTimer
The circular timer for iOS - KVTimer

![](https://s18.postimg.org/7iad1cgax/ezgif_com_video_to_gif.gif)


##Installation

### Using CocoaPods

KVTimer is available through [CocoaPods](http://cocoapods.org), to install
it simply add the following line to your Podfile:

    pod "KVTimer"

### Manual

Download the project and add the files `KVTimer.{h,m}` to your project.

##Usage
![](https://s10.postimg.org/xs26od095/ezgif_com_video_to_gif_2.gif)
  
    /*Create its Outlet -*/ @property (weak, nonatomic) IBOutlet KVTimer *timer;
 
    self.timer.delegate = self;
    [self.timer setShowTimerLabel:YES];
    [self.timer setMaxTime:120 minTime:0];
    self.timer.interval = KVIntervalSecond;
    
    KVStyle *style = [KVStyle initWithFillColor:[UIColor greenColor]
                                    strokeColor:[UIColor blackColor]
                                      lineWidth:2 radius:10];
    [self.timer setStylePin:<#(KVStyle *)#>]
    [self.timer setStyleLine:<#(KVStyle *)#>]
    [self.timer setStyleCircle:<#(KVStyle *)#>]
    
    [self.timer startTimer:/* YES / NO */];

###Method delegate:

    - (void)getTimer:(NSString *)time{
      NSLog(@"Time: %@", time);
    }
    
    - (void)endTime{
      NSLog(@"Oops:");
    }

## Author

Vlad Kochergin, kargod@ya.ru

## License

KVTimer is available under the MIT license. See the LICENSE file for more info.


