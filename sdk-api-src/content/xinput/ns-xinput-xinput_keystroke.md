---
UID: NS:xinput._XINPUT_KEYSTROKE
title: XINPUT_KEYSTROKE (xinput.h)
description: Specifies keystroke data returned by XInputGetKeystroke.
helpviewer_keywords: ["*PXINPUT_KEYSTROKE","PXINPUT_KEYSTROKE","PXINPUT_KEYSTROKE structure pointer [XInput Game Controller APIs]","XINPUT_KEYSTROKE","XINPUT_KEYSTROKE structure [XInput Game Controller APIs]","xinput.xinput_keystroke","xinput/PXINPUT_KEYSTROKE","xinput/XINPUT_KEYSTROKE"]
old-location: xinput\xinput_keystroke.htm
tech.root: xinput
ms.assetid: T:Microsoft.directx_sdk.reference.XINPUT_KEYSTROKE
ms.date: 12/05/2018
ms.keywords: '*PXINPUT_KEYSTROKE, PXINPUT_KEYSTROKE, PXINPUT_KEYSTROKE structure pointer [XInput Game Controller APIs], XINPUT_KEYSTROKE, XINPUT_KEYSTROKE structure [XInput Game Controller APIs], xinput.xinput_keystroke, xinput/PXINPUT_KEYSTROKE, xinput/XINPUT_KEYSTROKE'
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
req.typenames: XINPUT_KEYSTROKE, *PXINPUT_KEYSTROKE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XINPUT_KEYSTROKE
 - xinput/_XINPUT_KEYSTROKE
 - PXINPUT_KEYSTROKE
 - xinput/PXINPUT_KEYSTROKE
 - XINPUT_KEYSTROKE
 - xinput/XINPUT_KEYSTROKE
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
 - XINPUT_KEYSTROKE
---

# XINPUT_KEYSTROKE structure


## -description

Specifies keystroke data returned by <a href="/windows/desktop/api/xinput/nf-xinput-xinputgetkeystroke">XInputGetKeystroke</a>.

## -struct-fields

### -field VirtualKey

Virtual-key code of the key, button, or stick movement. See XInput.h for a list of valid virtual-key (VK_xxx) codes. Also, see Remarks.

### -field Unicode

This member is unused and the value is zero.

### -field Flags

Flags that indicate the keyboard state at the time of the input event. This member can be any combination of the following flags:        

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XINPUT_KEYSTROKE_KEYDOWN</td>
<td>The key was pressed. </td>
</tr>
<tr>
<td>XINPUT_KEYSTROKE_KEYUP</td>
<td>The key was released. </td>
</tr>
<tr>
<td>XINPUT_KEYSTROKE_REPEAT</td>
<td>A repeat of a held key. </td>
</tr>
</table>

### -field UserIndex

Index of the signed-in gamer associated with the device. Can be a value in the range 0–3.

### -field HidCode

HID code corresponding to the input. If there is no corresponding HID code, this value is zero.

## -remarks

Future devices may return HID codes and virtual key values that are not supported on current devices, and are currently undefined. Applications should ignore these unexpected values.



A <i>virtual-key</i> code is a byte value that represents a particular physical key on the keyboard, not the character or characters (possibly none) that the key can be mapped to based on keyboard state. The keyboard state at the time a virtual key is pressed modifies the character reported. For example, VK_4 might represent a "4" or a "$", depending on the state of the SHIFT key.



A reported keyboard event includes the virtual key that caused the event, whether the key was pressed or released (or is repeating), and the state of the keyboard at the time of the event. The keyboard state includes information about whether any CTRL, ALT, or SHIFT keys are down.



If the keyboard event represents an Unicode character (for example, pressing the "A" key), the <i>Unicode</i> member will contain that character. Otherwise, <i>Unicode</i> will contain the value zero.



The valid virtual-key (VK_xxx) codes are defined in XInput.h. In addition to codes that indicate key presses, the following codes indicate controller input.



<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>VK_PAD_A</td>
<td><b>A</b>  button </td>
</tr>
<tr>
<td>VK_PAD_B</td>
<td><b>B</b> button </td>
</tr>
<tr>
<td>VK_PAD_X</td>
<td><b>X</b> button </td>
</tr>
<tr>
<td>VK_PAD_Y</td>
<td><b>Y</b> button </td>
</tr>
<tr>
<td>VK_PAD_RSHOULDER</td>
<td>Right shoulder button </td>
</tr>
<tr>
<td>VK_PAD_LSHOULDER</td>
<td>Left shoulder button </td>
</tr>
<tr>
<td>VK_PAD_LTRIGGER</td>
<td>Left trigger </td>
</tr>
<tr>
<td>VK_PAD_RTRIGGER</td>
<td>Right trigger </td>
</tr>
<tr>
<td>VK_PAD_DPAD_UP</td>
<td>Directional pad up </td>
</tr>
<tr>
<td>VK_PAD_DPAD_DOWN</td>
<td>Directional pad down </td>
</tr>
<tr>
<td>VK_PAD_DPAD_LEFT</td>
<td>Directional pad left </td>
</tr>
<tr>
<td>VK_PAD_DPAD_RIGHT</td>
<td>Directional pad right </td>
</tr>
<tr>
<td>VK_PAD_START</td>
<td><b>START</b> button </td>
</tr>
<tr>
<td>VK_PAD_BACK</td>
<td><b>BACK</b> button </td>
</tr>
<tr>
<td>VK_PAD_LTHUMB_PRESS</td>
<td>Left thumbstick click </td>
</tr>
<tr>
<td>VK_PAD_RTHUMB_PRESS</td>
<td>Right thumbstick click </td>
</tr>
<tr>
<td>VK_PAD_LTHUMB_UP</td>
<td>Left thumbstick up </td>
</tr>
<tr>
<td>VK_PAD_LTHUMB_DOWN</td>
<td>Left thumbstick down </td>
</tr>
<tr>
<td>VK_PAD_LTHUMB_RIGHT</td>
<td>Left thumbstick right </td>
</tr>
<tr>
<td>VK_PAD_LTHUMB_LEFT</td>
<td>Left thumbstick left </td>
</tr>
<tr>
<td>VK_PAD_LTHUMB_UPLEFT</td>
<td>Left thumbstick up and left </td>
</tr>
<tr>
<td>VK_PAD_LTHUMB_UPRIGHT</td>
<td>Left thumbstick up and right </td>
</tr>
<tr>
<td>VK_PAD_LTHUMB_DOWNRIGHT</td>
<td>Left thumbstick down and right </td>
</tr>
<tr>
<td>VK_PAD_LTHUMB_DOWNLEFT</td>
<td>Left thumbstick down and left </td>
</tr>
<tr>
<td>VK_PAD_RTHUMB_UP</td>
<td>Right thumbstick up </td>
</tr>
<tr>
<td>VK_PAD_RTHUMB_DOWN</td>
<td>Right thumbstick down </td>
</tr>
<tr>
<td>VK_PAD_RTHUMB_RIGHT</td>
<td>Right thumbstick right </td>
</tr>
<tr>
<td>VK_PAD_RTHUMB_LEFT</td>
<td>Right thumbstick left </td>
</tr>
<tr>
<td>VK_PAD_RTHUMB_UPLEFT</td>
<td>Right thumbstick up and left </td>
</tr>
<tr>
<td>VK_PAD_RTHUMB_UPRIGHT</td>
<td>Right thumbstick up and right </td>
</tr>
<tr>
<td>VK_PAD_RTHUMB_DOWNRIGHT</td>
<td>Right thumbstick down and right </td>
</tr>
<tr>
<td>VK_PAD_RTHUMB_DOWNLEFT</td>
<td>Right thumbstick down and left </td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetkeystroke">XInputGetKeystroke</a>