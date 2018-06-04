---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _MOUSE_ATTRIBUTES structure


## -description


MOUSE_ATTRIBUTES specifies the attributes of a mouse device.


## -struct-fields




### -field MouseIdentifier

Specifies one of the following types of mouse devices.

<table>
<tr>
<th>Mouse type</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BALLPOINT_I8042_HARDWARE

</td>
<td>
i8042 port ballpoint mouse

</td>
</tr>
<tr>
<td>
BALLPOINT_SERIAL_HARDWARE

</td>
<td>
Serial port ballpoint mouse

</td>
</tr>
<tr>
<td>
MOUSE_HID_HARDWARE

</td>
<td>
HIDClass mouse

</td>
</tr>
<tr>
<td>
MOUSE_I8042_HARDWARE

</td>
<td>
i8042 port mouse

</td>
</tr>
<tr>
<td>
MOUSE_INPORT_HARDWARE

</td>
<td>
Inport (bus) mouse

</td>
</tr>
<tr>
<td>
MOUSE_SERIAL_HARDWARE

</td>
<td>
Serial port mouse

</td>
</tr>
<tr>
<td>
WHEELMOUSE_HID_HARDWARE

</td>
<td>
HIDClass wheel mouse

</td>
</tr>
<tr>
<td>
WHEELMOUSE_I8042_HARDWARE

</td>
<td>
i8042 port wheel mouse

</td>
</tr>
<tr>
<td>
WHEELMOUSE_SERIAL_HARDWARE

</td>
<td>
Serial port wheel mouse

</td>
</tr>
</table>
 


### -field NumberOfButtons

Specifies the number of buttons supported by a mouse. A mouse can have from two to five buttons. The default value is MOUSE_NUMBER_OF_BUTTONS. 


### -field SampleRate

Specifies the rate, in reports per second, at which input from a PS/2 mouse is sampled. The default value is MOUSE_SAMPLE_RATE. This value is not used for USB devices.


### -field InputDataQueueLength

Specifies the size, in bytes, of the input data queue used by the port driver for a mouse device. 


## -remarks



This structure is used with an <a href="https://msdn.microsoft.com/library/windows/hardware/ff542080">IOCTL_MOUSE_QUERY_ATTRIBUTES</a> request to obtain the attributes of a mouse. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff542080">IOCTL_MOUSE_QUERY_ATTRIBUTES</a>
 

 

