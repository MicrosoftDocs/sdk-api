---
UID: NS:xinput._XINPUT_GAMEPAD
title: XINPUT_GAMEPAD (xinput.h)
description: Describes the current state of the controller.
helpviewer_keywords: ["*PXINPUT_GAMEPAD","PXINPUT_GAMEPAD","PXINPUT_GAMEPAD structure pointer [XInput Game Controller APIs]","XINPUT_GAMEPAD","XINPUT_GAMEPAD structure [XInput Game Controller APIs]","xinput.xinput_gamepad","xinput/PXINPUT_GAMEPAD","xinput/XINPUT_GAMEPAD"]
old-location: xinput\xinput_gamepad.htm
tech.root: xinput
ms.assetid: T:Microsoft.directx_sdk.reference.XINPUT_GAMEPAD
ms.date: 12/05/2018
ms.keywords: '*PXINPUT_GAMEPAD, PXINPUT_GAMEPAD, PXINPUT_GAMEPAD structure pointer [XInput Game Controller APIs], XINPUT_GAMEPAD, XINPUT_GAMEPAD structure [XInput Game Controller APIs], xinput.xinput_gamepad, xinput/PXINPUT_GAMEPAD, xinput/XINPUT_GAMEPAD'
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
req.typenames: XINPUT_GAMEPAD, *PXINPUT_GAMEPAD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XINPUT_GAMEPAD
 - xinput/_XINPUT_GAMEPAD
 - PXINPUT_GAMEPAD
 - xinput/PXINPUT_GAMEPAD
 - XINPUT_GAMEPAD
 - xinput/XINPUT_GAMEPAD
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
 - XINPUT_GAMEPAD
---

# XINPUT_GAMEPAD structure


## -description

Describes the current state of the controller.

## -struct-fields

### -field wButtons

Bitmask of the device digital buttons, as follows. A set bit indicates that the corresponding button is pressed. 
        

<table>
<tr>
<th>Device button</th>
<th>Bitmask</th>
</tr>
<tr>
<td>XINPUT_GAMEPAD_DPAD_UP</td>
<td> 0x0001</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_DPAD_DOWN</td>
<td>        0x0002</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_DPAD_LEFT</td>
<td>       0x0004</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_DPAD_RIGHT</td>
<td>      0x0008</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_START</td>
<td>          0x0010</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_BACK</td>
<td>             0x0020</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_LEFT_THUMB</td>
<td>       0x0040</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_RIGHT_THUMB</td>
<td>      0x0080</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_LEFT_SHOULDER</td>
<td>    0x0100</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_RIGHT_SHOULDER</td>
<td>   0x0200</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_A</td>
<td>                0x1000</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_B</td>
<td>                0x2000</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_X</td>
<td>                0x4000</td>
</tr>
<tr>
<td>XINPUT_GAMEPAD_Y</td>
<td>                0x8000</td>
</tr>
</table>
 

Bits that are set but not defined above are reserved, and their state is undefined.

### -field bLeftTrigger

The current value of the left trigger analog control. The value is between 0 and 255.

### -field bRightTrigger

The current value of the right trigger analog control. The value is between 0 and 255.

### -field sThumbLX

Left thumbstick x-axis value. Each of the thumbstick axis members is a signed value between -32768 and 32767 describing the position of the thumbstick. A value of 0 is centered. Negative values signify down or to the left. Positive values signify up or to the right. The constants XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE or XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE can be used as a positive and negative value to filter a thumbstick input.

### -field sThumbLY

Left thumbstick y-axis value. The value is between -32768 and 32767.

### -field sThumbRX

Right thumbstick x-axis value. The value is between -32768 and 32767.

### -field sThumbRY

Right thumbstick y-axis value. The value is between -32768 and 32767.

## -remarks

This structure is used by the <a href="/windows/desktop/api/xinput/ns-xinput-xinput_state">XINPUT_STATE</a> structure when polling for changes in the state of the controller.



The specific mapping of button to game function varies depending on the game type.



The constant XINPUT_GAMEPAD_TRIGGER_THRESHOLD may be used as the value which <i>bLeftTrigger</i> and <i>bRightTrigger</i> must be greater than to register as pressed. This is optional, but often desirable. Controller buttons do not manifest crosstalk.

## -see-also

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_state">XINPUT_STATE</a>



<a href="/windows/desktop/xinput/structures">XInput Structures</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetstate">XInputGetState</a>
