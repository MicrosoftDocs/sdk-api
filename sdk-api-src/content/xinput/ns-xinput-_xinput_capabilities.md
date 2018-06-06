---
UID: NS:xinput._XINPUT_CAPABILITIES
title: "_XINPUT_CAPABILITIES"
author: windows-sdk-content
description: Describes the capabilities of a connected controller. The XInputGetCapabilities function returns XINPUT_CAPABILITIES.
old-location: xinput\xinput_capabilities.htm
old-project: xinput
ms.assetid: T:Microsoft.directx_sdk.reference.XINPUT_CAPABILITIES
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PXINPUT_CAPABILITIES, PXINPUT_CAPABILITIES, PXINPUT_CAPABILITIES structure pointer [XInput Game Controller APIs], XINPUT_CAPABILITIES, XINPUT_CAPABILITIES structure [XInput Game Controller APIs], _XINPUT_CAPABILITIES, xinput.xinput_capabilities, xinput/PXINPUT_CAPABILITIES, xinput/XINPUT_CAPABILITIES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xinput.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: XINPUT_CAPABILITIES, *PXINPUT_CAPABILITIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - XInput.h
api_name:
 - XINPUT_CAPABILITIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# _XINPUT_CAPABILITIES structure


## -description


Describes the capabilities of a connected controller. The <a href="https://msdn.microsoft.com/5F02EFF5-57ED-4FF1-88E2-DB1CB6F33151">XInputGetCapabilities</a> function returns <b>XINPUT_CAPABILITIES</b>. 


## -struct-fields




### -field Type

      
       Controller type. It must be one of the following values.
       

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XINPUT_DEVTYPE_GAMEPAD</td>
<td>The device is a game controller. </td>
</tr>
</table>
 


### -field SubType

Subtype of the game controller. See <a href="https://msdn.microsoft.com/4674028b-98cf-5346-7b93-f940150f3051">XINPUT and Controller Subtypes</a> for a list of allowed subtypes.

<div class="alert"><b>Note</b>  For restrictions on the use of this subtype value, see Remarks. More subtypes may be added in the future.</div>
<div> </div>

### -field Flags

Features of the controller.
       

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XINPUT_CAPS_VOICE_SUPPORTED</td>
<td>Device has an integrated voice device.</td>
</tr>
<tr>
<td>XINPUT_CAPS_FFB_SUPPORTED</td>
<td>Device supports force feedback functionality. Note that these force-feedback features beyond rumble are not currently supported through XINPUT on Windows.</td>
</tr>
<tr>
<td>XINPUT_CAPS_WIRELESS</td>
<td>Device is wireless.</td>
</tr>
<tr>
<td>XINPUT_CAPS_PMD_SUPPORTED</td>
<td>
           Device supports plug-in modules. Note that plug-in modules like the text input device (TID)
           are not supported currently through XINPUT on Windows.</td>
</tr>
<tr>
<td>XINPUT_CAPS_NO_NAVIGATION</td>
<td>Device lacks menu navigation buttons (START, BACK, DPAD).</td>
</tr>
</table>
 


### -field Gamepad


<a href="https://msdn.microsoft.com/9F3BA764-82E0-4C46-AAA3-F417D2344ECB">XINPUT_GAMEPAD</a> structure that describes available controller features and control resolutions. 


### -field Vibration


<a href="https://msdn.microsoft.com/134A22DD-95DA-4270-AC42-93C7EF110A3A">XINPUT_VIBRATION</a> structure that describes available vibration functionality and resolutions.


## -remarks




<a href="https://msdn.microsoft.com/5F02EFF5-57ED-4FF1-88E2-DB1CB6F33151">XInputGetCapabilities</a> returns <b>XINPUT_CAPABILITIES</b> to indicate the characteristics and available functionality of a specified controller.




<a href="https://msdn.microsoft.com/5F02EFF5-57ED-4FF1-88E2-DB1CB6F33151">XInputGetCapabilities</a> sets the structure members to indicate which inputs the device supports. For binary state controls, such as digital buttons, the corresponding bit reflects whether or not the control is supported by the device. For proportional controls, such as thumbsticks, the value indicates the resolution for that control. Some number of the least significant bits may not be set, indicating that the control does not provide resolution to that level.



The <i>SubType</i> member indicates the specific subtype of controller present. Games may detect the controller subtype and tune their handling of controller input or output based on subtypes that are well suited to their game genre. For example, a car racing game might check for the presence of a wheel controller to provide finer control of the car being driven. However, titles must not disable or ignore a device based on its subtype. Subtypes not recognized by the game or for which the game is not specifically tuned should be treated as a standard Xbox 360 Controller (XINPUT_DEVSUBTYPE_GAMEPAD).



Older XUSB Windows drivers report incomplete capabilities information, particularly for wireless devices. The latest XUSB Windows driver provides full support for wired and wireless devices, and more complete and accurate capabilties flags.






## -see-also




<a href="https://msdn.microsoft.com/9F3BA764-82E0-4C46-AAA3-F417D2344ECB">XINPUT_GAMEPAD</a>



<a href="https://msdn.microsoft.com/134A22DD-95DA-4270-AC42-93C7EF110A3A">XINPUT_VIBRATION</a>



<a href="https://msdn.microsoft.com/89bb00ea-0be3-9619-1629-a7b7894302d5">XInput Structures</a>



<a href="https://msdn.microsoft.com/5F02EFF5-57ED-4FF1-88E2-DB1CB6F33151">XInputGetCapabilities</a>
 

 

