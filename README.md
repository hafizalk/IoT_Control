This flow is half of the Overall IoT based Control Infrastructure to enable the Remote Tele-Operation of a Vehicle.

The json flow creates a Node-Red User Interface which serves as the Control plaftorm for the Operator to pilot the vehicle. The flow uses a USB HID node to extract the control data (button press) for the vehicle from the Operator using an XBox 360 controller gamepad connected through USB to the host computer running the node-red flow. The data is processed within the flow into a suitable format and sent using an MQTT Output node over an MQTT server hosted by AWS (Amazon Web Services) IOT thing, to the receiver side node-red flow running on a raspberry pi embedded on the vehicle.

The flow utlizes some User contributed node-red nodes such as: 
USBHID; 
Node-Red Dashboard nodes for the User Interface (UI). 
Other nodes utlized are standard node-red nodes available on installation.