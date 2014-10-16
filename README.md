upgrade to support phonegap 3.0.0

because it need to open local file. if you want to open remote file via url,
you should download the file to local directory.

so you need to install plugins:

cordova-plugin-file
cordova-plugin-file-transfer


to downlaod from file you could visit http://mythoughtsandexperiments.blogspot.jp/2013/10/phonegap-file-downloading-and.html

for using phonegap-plugin-ios-quick-look, you could using 



var fullpath="your.file.fullpath";
cordova.exec(

	function() { return; },

	function() { return; },

	"QuickLookPlugin", "quickLookFile", [fullpath]

);


The Phonegap Quick Look plugin provides a way to open documents, images and text files (e.g. iWorks, PDF, Word, Excel, Powerpoint, PNG, JPEG, rich text, CSV) directly from your iOS application (e.g. iPhone or iPad). The plugin uses the Quick Look functionality of iOS (https://developer.apple.com/library/ios/documentation/FileManagement/Conceptual/DocumentInteraction_TopicsForIOS/Articles/UsingtheQuickLookFramework.html). The user doesn't need a program for that specific file format. The framework also supports 'forwarding' the file to any other application on the device that supports that file format.
