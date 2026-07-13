---
UID: NS:xinput._XINPUT_CAPABILITIES
title: XINPUT_CAPABILITIES (xinput.h)
description: Describes the capabilities of a connected controller. The XInputGetCapabilities function returns XINPUT_CAPABILITIES.
helpviewer_keywords: ["*PXINPUT_CAPABILITIES","PXINPUT_CAPABILITIES","PXINPUT_CAPABILITIES structure pointer [XInput Game Controller APIs]","XINPUT_CAPABILITIES","XINPUT_CAPABILITIES structure [XInput Game Controller APIs]","xinput.xinput_capabilities","xinput/PXINPUT_CAPABILITIES","xinput/XINPUT_CAPABILITIES"]
old-location: xinput\xinput_capabilities.htm
tech.root: xinput
ms.assetid: T:Microsoft.directx_sdk.reference.XINPUT_CAPABILITIES
ms.date: 12/05/2018
ms.keywords: '*PXINPUT_CAPABILITIES, PXINPUT_CAPABILITIES, PXINPUT_CAPABILITIES structure pointer [XInput Game Controller APIs], XINPUT_CAPABILITIES, XINPUT_CAPABILITIES structure [XInput Game Controller APIs], xinput.xinput_capabilities, xinput/PXINPUT_CAPABILITIES, xinput/XINPUT_CAPABILITIES'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XINPUT_CAPABILITIES, *PXINPUT_CAPABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XINPUT_CAPABILITIES
 - xinput/_XINPUT_CAPABILITIES
 - PXINPUT_CAPABILITIES
 - xinput/PXINPUT_CAPABILITIES
 - XINPUT_CAPABILITIES
 - xinput/XINPUT_CAPABILITIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - XInput.h
api_name:
 - XINPUT_CAPABILITIES
---

# XINPUT_CAPABILITIES structure


## -description

Describes the capabilities of a connected controller. The <a href="/windows/desktop/api/xinput/nf-xinput-xinputgetcapabilities">XInputGetCapabilities</a> function returns <b>XINPUT_CAPABILITIES</b>.

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

Subtype of the game controller. See <a href="/windows/desktop/xinput/xinput-and-controller-subtypes">XINPUT and Controller Subtypes</a> for a list of allowed subtypes.

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
<td>Device supports plug-in modules. Note that plug-in modules like the text input device (TID)
           are not supported currently through XINPUT on Windows.</td>
</tr>
<tr>
<td>XINPUT_CAPS_NO_NAVIGATION</td>
<td>Device lacks menu navigation buttons (START, BACK, DPAD).</td>
</tr>
</table>

### -field Gamepad

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_gamepad">XINPUT_GAMEPAD</a> structure that describes available controller features and control resolutions.

### -field Vibration

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_vibration">XINPUT_VIBRATION</a> structure that describes available vibration functionality and resolutions.

## -remarks

<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetcapabilities">XInputGetCapabilities</a> returns <b>XINPUT_CAPABILITIES</b> to indicate the characteristics and available functionality of a specified controller.




<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetcapabilities">XInputGetCapabilities</a> sets the structure members to indicate which inputs the device supports. For binary state controls, such as digital buttons, the corresponding bit reflects whether or not the control is supported by the device. For proportional controls, such as thumbsticks, the value indicates the resolution for that control. Some number of the least significant bits may not be set, indicating that the control does not provide resolution to that level.



The <i>SubType</i> member indicates the specific subtype of controller present. Games may detect the controller subtype and tune their handling of controller input or output based on subtypes that are well suited to their game genre. For example, a car racing game might check for the presence of a wheel controller to provide finer control of the car being driven. However, titles must not disable or ignore a device based on its subtype. Subtypes not recognized by the game or for which the game is not specifically tuned should be treated as a standard controller (XINPUT_DEVSUBTYPE_GAMEPAD).



Older XUSB Windows drivers report incomplete capabilities information, particularly for wireless devices. The latest XUSB Windows driver provides full support for wired and wireless devices, and more complete and accurate capabilities flags.

## -see-also

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_gamepad">XINPUT_GAMEPAD</a>



<a href="/windows/desktop/api/xinput/ns-xinput-xinput_vibration">XINPUT_VIBRATION</a>



<a href="/windows/desktop/xinput/structures">XInput Structures</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetcapabilities">XInputGetCapabilities</a>