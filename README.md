musiclabel
==========

xcode tutorial for parse website

// cargar canciones 

en el .m


    soundFile = [NSURL fileURLWithPath:[[NSBundle mainBundle]
                       pathForResource:@"keinelust" ofType:@"wav"]];
    
    sound = [[AVAudioPlayer alloc] initWithContentsOfURL:soundFile error:nil];
    sound.delegate = self;
    
    
//para reproducir

[sound.Play];

//en el .h


#import <UIKit/UIKit.h>
#import <AVFoundation/AVAudioPlayer.h>
#import <AudioToolbox/AudioToolbox.h>

@interface ViewController : UIViewController
{

    NSURL *soundFile;
    AVAudioPlayer *sound;
}
