symptomChecker
==============

a Html/Javascript/jQuery Mobile interface that interacts with server-side Clips interface using HTML5 WebSockets. 
The interface is PhoneGap packaged as an Android App (Eye CheckApp) and is available to download here:
https://play.google.com/store/apps/details?id=com.phonegap.eyechekapp 
Demo
----
Check demo here (hosted in Amazon Web Services in an EC2 Ubuntu instance): http://54.194.22.198/eyeCheckApp/eyeCheckApp/ (multilingual).
Details
-------
server-side controller takes advantage of websocketd project (https://github.com/joewalnes/websocketd/) to wrap the CLIPS interface to a WebSocket interface.
In order to start server-side CLIPS interface execute:
./websocketd --port=8088 /Applications/CLIPS/./clips -f troubleshooter.clp
where 8088 is the desired port /Applications/CLIPS/./clips is the path to the clips executable and troubleshooter.clp is the clips source.

In order to start the server and then close the terminal execute:
nohup loop_troubleshooter.sh &

Download the right version of webSocketd from https://github.com/joewalnes/websocketd/wiki/Download-and-install