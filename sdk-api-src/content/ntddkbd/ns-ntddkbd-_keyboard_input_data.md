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

# _KEYBOARD_INPUT_DATA structure


## -description


KEYBOARD_INPUT_DATA contains one packet of keyboard input data.


## -struct-fields




### -field UnitId

Specifies the unit number of a keyboard device. A keyboard device name has the format \Device\KeyboardPort<i>N</i>, where the suffix <i>N </i>is the unit number of the device. For example, a device, whose name is \Device\KeyboardPort0, has a unit number of zero, and a device, whose name is \Device\KeyboardPort1, has a unit number of one. 


### -field MakeCode

Specifies the scan code associated with a key press.


### -field Flags

Specifies a bitwise OR of one or more of the following flags that indicate whether a key was pressed or released, and other miscellaneous information.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
KEY_MAKE

</td>
<td>
The key was pressed.

</td>
</tr>
<tr>
<td>
KEY_BREAK

</td>
<td>
The key was released.

</td>
</tr>
<tr>
<td>
KEY_E0

</td>
<td>
Extended scan code used to indicate special keyboard functions. 

</td>
</tr>
<tr>
<td>
KEY_E1

</td>
<td>
Extended scan code used to indicate special keyboard functions. 

</td>
</tr>
</table>
 


### -field Reserved

Reserved for operating system use.


### -field ExtraInformation

Specifies device-specific information associated with a keyboard event.


## -remarks



In response to an <a href="https://msdn.microsoft.com/9b009d0a-6654-4fed-99d7-c0fd3fb0fb33">IRP_MJ_READ (Kbdclass)</a> request, Kbdclass transfers zero or more <b>KEYBOARD_INPUT_DATA</b> structures from its internal data queue to the Win32 subsystem buffer.




## -see-also




<a href="https://msdn.microsoft.com/9b009d0a-6654-4fed-99d7-c0fd3fb0fb33">IRP_MJ_READ (Kbdclass)</a>



<a href="https://msdn.microsoft.com/02815805-47cf-454c-8117-f5686a855e25">KeyboardClassServiceCallback</a>
 

 

