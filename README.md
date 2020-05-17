# Strokes
## WWDC 2020 Swift Challenge Submission

For my Swift Challenge Submission this year, I made Strokes. Strokes is a stroke detector and raises awareness about the deadly yet preventable effects of stroke. I’ve lost a couple of my close family members to this deadly disease and later when I studied about it I realized how much could’ve been prevented if correct measures were taken at the right time. This Swift playground attempts to help understand the importance of understanding the effects, diagnostic options, and what to do in case of a stroke.

![Image description](https://github.com/SwapnanilDhol/Strokes/blob/master/image.png?raw=true)

### Technologies Used:

- **RealityKit**: RealityKit is a powerful new API that was introduced in WWDC 2019 that builds upon the power of ARKit. The ARM Drop Screen uses RealityKit by analysing different anchor points provided by the BodySkeleton method. I track the positions of the two hands relative to the body and track their position in real time to determine the positon of the hands in space. After a lot of tinkering I came up with values that I check against to determine if the hands are raised or have started to drift down. When the user raises both hands, a timer is started that ticks till 5 seconds and then analyses the position values over that time and returns a result based on that. 

- **ARKit**: The Face Drop Analyzer screen uses the ARKit Framework to attach anchor points to a 3D result of a face using the True Depth camera. The playground then analyses the value of the lower jaw anchor points to check if any side of the face has dropped during the analysis period. 

- **SwiftUI**: Strokes uses SwiftUI in two pages: The initial Information screen and the end quiz screen. It was super fun and easy to build UI and attach them with logic using this framework. I literally had 2 of my playground pages ready in a day.
- **CreateML**: The speech detector screen uses a custom trained ML Model that I trained using the brand new CreateML app and especially the sound classification feature. The dataset was custom made using voices I found around me and of myself.
- **CoreML**:  The speech analysis is done using CoreML that uses the custom MLModel generated using CreateML
