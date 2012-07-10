# videotracker.js

An javascript video tracker.

The object tracking is based in color detection and blend difference.
The color detection algorimth is using hsv colour to extract  color selected areas in the picture combined with a blend mode to capture only the objects with movement.
Although this method is not very stable, is an efficient way to detect objects using a javascript browser engine, the contextual environment had significant influence on the accuracy of the results but configuring carefully the color range and the environment it can be a good way for tracking objects.

 * No plugins, only javascript
 * No dependencies
 * Highly configurable
 * Small footprint (~1.9K gzipped)
 * MIT License

## Usage

```javascript
onMoveFunc = function(x,y){
  alert('Object detected!!');
};
var videotracker = new VideoTracker({video_target_id: 'video_id'});
videotracker.setOnMoveFunc(onMoveFunc);
videotracker.start();
```

For an interactive demo and a list of all supported options please refer to the [project's homepage](http://lusob.github.com/videotracker.js).