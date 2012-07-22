# Ti iSimulate Module

![iSimulate Image](http://www.vimov.com/images/10/isimulate/header-banner-02.png)

## Description

iSimulate is an application/library pair designed to solve the issue of not being able to use multi-touch, the accelerometer and compass in the iOS Simulator. Now, with iSimulate on your iPhone, iPad or iPod Touch, it will wirelessly send multi-touch events, the accelerometer and compass events, and the GPS location to the iOS Simulator.

This module brings iSimulate into your Titanium project for testing accelerometer events in the simulator using your device.

Read more about iSimulate here: http://www.vimov.com/isimulate/documentation/
http://www.vimov.com/images/10/isimulate/doc-screenshot-01.jpg
## Accessing the Ti iSimulate Module

To use this module, you will need to download iSimulate iPhone app from the Apple App Store.  Then you must install this TiSimulate module in your Titanium project.

1. Simply add the module to tiapp.xml, clean your project and run the simulator from Titanium. 
2. Run the iSimulate mobile client on your iOS device. You should see your computer listed as a source to connect.

Note: There is no need to explicitly invoke the JavaScript require() method in your Titanium project.  This module wraps the iSimulate SDK library directly to CoreLocation and will be compiled as part of your app project.

You may want to add this to the global module directory:
~/Library/Application Support/Titanium/modules

## FAQs

### How does iSimulate work?
When added to your project, the iSimulate SDK library creates a listening server on your iPhone Simulator that waits for a connection from an iPhone/iPod running the iSimulate client. When such connection is established, the iSimulate client running on your iPhone/iPod captures all data from the accelerometer sensor, the touch events, the location and device ID and streams them to the server. The iSimulate SDK library then recreates all input events synthetically. This is entirely transparent to your application and does not interfere with your application's functionality.

### Will the iSimulate SDK library be linked into my released application?
No, the iSimulate SDK library will be linked to only when the application is compiled for the iPhone Simulator. When you build the application and install it on a device, the iSimulate SDK would not have been compiled into it.

### How does iSimulate connect to the iPhone Simulator?
iSimulate requires that both your iPhone/iPod be connected on the same wireless network. If not, you will need to create an Adhoc network (computer-to-computer network) on your Mac and connect to it from your iPhone/iPod. Adhoc connections have been reported to have less performance than WiFi connections through a router if you're using 3.0 on an iPhone (iPods not affected).

## Reference

http:/  www.vimov.com/isimulate/documentation/

## Author

Terry Martin, Semantic Press
http://twitter.com/tzmartin
martin@semanticpress.com

## License

Copyright (c) 2012 Terry Martin

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
