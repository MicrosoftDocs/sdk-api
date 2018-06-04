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

# _XINPUT_GAMEPAD structure


## -description


Describes the current state of the Xbox 360 Controller.


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



This structure is used by the <a href="https://msdn.microsoft.com/1EBFB5FF-3DAA-43D8-AADA-5FFEED56F79D">XINPUT_STATE</a> structure when polling for changes in the state of the controller.



The specific mapping of button to game function varies depending on the game type.



The constant XINPUT_GAMEPAD_TRIGGER_THRESHOLD may be used as the value which <i>bLeftTrigger</i> and <i>bRightTrigger</i> must be greater than to register as pressed. This is optional, but often desirable. Xbox 360 Controller buttons do not manifest crosstalk.





## -see-also




<a href="https://msdn.microsoft.com/1EBFB5FF-3DAA-43D8-AADA-5FFEED56F79D">XINPUT_STATE</a>



<a href="https://msdn.microsoft.com/89bb00ea-0be3-9619-1629-a7b7894302d5">XInput Structures</a>



<a href="https://msdn.microsoft.com/D261219D-0175-4690-8F1F-BDAACE2E7424">XInputGetfState</a>
 

 

