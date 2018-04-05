---
UID: NS:wincon._MOUSE_EVENT_RECORD
title: "_MOUSE_EVENT_RECORD"
author: windows-driver-content
description: Describes a mouse input event in a console INPUT_RECORD structure.
old-location: consoles\mouse_event_record_str.htm
old-project: consoles
ms.assetid: 84ea54c6-8872-4111-8d72-1377409b9247
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PMOUSE_EVENT_RECORD, CAPSLOCK_ON, DOUBLE_CLICK, ENHANCED_KEY, FROM_LEFT_1ST_BUTTON_PRESSED, FROM_LEFT_2ND_BUTTON_PRESSED, FROM_LEFT_3RD_BUTTON_PRESSED, FROM_LEFT_4TH_BUTTON_PRESSED, LEFT_ALT_PRESSED, LEFT_CTRL_PRESSED, MOUSE_EVENT_RECORD, MOUSE_EVENT_RECORD structure [Consoles], MOUSE_HWHEELED, MOUSE_MOVED, MOUSE_WHEELED, NUMLOCK_ON, RIGHTMOST_BUTTON_PRESSED, RIGHT_ALT_PRESSED, RIGHT_CTRL_PRESSED, SCROLLLOCK_ON, SHIFT_PRESSED, _MOUSE_EVENT_RECORD, _win32_mouse_event_record_str, base.mouse_event_record_str, consoles.mouse_event_record_str, wincon/MOUSE_EVENT_RECORD"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MOUSE_EVENT_RECORD, *PMOUSE_EVENT_RECORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	MOUSE_EVENT_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _MOUSE_EVENT_RECORD structure


## -description


Describes a mouse input event in a console 
<a href="https://msdn.microsoft.com/a46ba7fd-097a-455d-96ac-13aa01e11dc1">INPUT_RECORD</a> structure.


## -struct-fields




### -field dwMousePosition

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that contains the location of the cursor, in terms of the console screen buffer's character-cell coordinates.


### -field dwButtonState

The status of the mouse buttons. The least significant bit corresponds to the leftmost mouse button. The next least significant bit corresponds to the rightmost mouse button. The next bit indicates the next-to-leftmost mouse button. The bits then correspond left to right to the mouse buttons. A bit is 1 if the button was pressed.

The following constants are defined for the first five mouse buttons.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FROM_LEFT_1ST_BUTTON_PRESSED"></a><a id="from_left_1st_button_pressed"></a><dl>
<dt><b>FROM_LEFT_1ST_BUTTON_PRESSED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The leftmost mouse button.

</td>
</tr>
<tr>
<td width="40%"><a id="FROM_LEFT_2ND_BUTTON_PRESSED"></a><a id="from_left_2nd_button_pressed"></a><dl>
<dt><b>FROM_LEFT_2ND_BUTTON_PRESSED</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The second button from the left.

</td>
</tr>
<tr>
<td width="40%"><a id="FROM_LEFT_3RD_BUTTON_PRESSED"></a><a id="from_left_3rd_button_pressed"></a><dl>
<dt><b>FROM_LEFT_3RD_BUTTON_PRESSED</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The third button from the left.

</td>
</tr>
<tr>
<td width="40%"><a id="FROM_LEFT_4TH_BUTTON_PRESSED"></a><a id="from_left_4th_button_pressed"></a><dl>
<dt><b>FROM_LEFT_4TH_BUTTON_PRESSED</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The fourth button from the left.

</td>
</tr>
<tr>
<td width="40%"><a id="RIGHTMOST_BUTTON_PRESSED"></a><a id="rightmost_button_pressed"></a><dl>
<dt><b>RIGHTMOST_BUTTON_PRESSED</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The rightmost mouse button.

</td>
</tr>
</table>
 


### -field dwControlKeyState

The state of the control keys. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CAPSLOCK_ON"></a><a id="capslock_on"></a><dl>
<dt><b>CAPSLOCK_ON</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
The CAPS LOCK light is on.

</td>
</tr>
<tr>
<td width="40%"><a id="ENHANCED_KEY"></a><a id="enhanced_key"></a><dl>
<dt><b>ENHANCED_KEY</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
The key is enhanced.

</td>
</tr>
<tr>
<td width="40%"><a id="LEFT_ALT_PRESSED"></a><a id="left_alt_pressed"></a><dl>
<dt><b>LEFT_ALT_PRESSED</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The left ALT key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="LEFT_CTRL_PRESSED"></a><a id="left_ctrl_pressed"></a><dl>
<dt><b>LEFT_CTRL_PRESSED</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The left CTRL key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="NUMLOCK_ON"></a><a id="numlock_on"></a><dl>
<dt><b>NUMLOCK_ON</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The NUM LOCK light is on.

</td>
</tr>
<tr>
<td width="40%"><a id="RIGHT_ALT_PRESSED"></a><a id="right_alt_pressed"></a><dl>
<dt><b>RIGHT_ALT_PRESSED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The right ALT key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="RIGHT_CTRL_PRESSED"></a><a id="right_ctrl_pressed"></a><dl>
<dt><b>RIGHT_CTRL_PRESSED</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The right CTRL key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="SCROLLLOCK_ON"></a><a id="scrolllock_on"></a><dl>
<dt><b>SCROLLLOCK_ON</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
The SCROLL LOCK light is on.

</td>
</tr>
<tr>
<td width="40%"><a id="SHIFT_PRESSED"></a><a id="shift_pressed"></a><dl>
<dt><b>SHIFT_PRESSED</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The SHIFT key is pressed.

</td>
</tr>
</table>
 


### -field dwEventFlags

The type of mouse event. If this value is zero, it indicates a mouse button being pressed or released. Otherwise, this member is one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DOUBLE_CLICK"></a><a id="double_click"></a><dl>
<dt><b>DOUBLE_CLICK</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The second click (button press) of a double-click occurred. The first click is returned as a regular button-press event.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSE_HWHEELED"></a><a id="mouse_hwheeled"></a><dl>
<dt><b>MOUSE_HWHEELED</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The horizontal mouse wheel was moved.

If the high word of the <b>dwButtonState</b> member contains a positive value, the wheel was rotated to the right. Otherwise, the wheel was rotated to the left.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSE_MOVED"></a><a id="mouse_moved"></a><dl>
<dt><b>MOUSE_MOVED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
A change in mouse position occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSE_WHEELED"></a><a id="mouse_wheeled"></a><dl>
<dt><b>MOUSE_WHEELED</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The vertical mouse wheel was moved.

If the high word of the <b>dwButtonState</b> member contains a positive value, the wheel was rotated forward, away from the user. Otherwise, the wheel was rotated backward, toward the user.

</td>
</tr>
</table>
 


## -remarks



Mouse events are placed in the input buffer when the console is in mouse mode (<b>ENABLE_MOUSE_INPUT</b>).

Mouse events are generated whenever the user moves the mouse, or presses or releases one of the mouse buttons. Mouse events are placed in a console's input buffer only when the console group has the keyboard focus and the cursor is within the borders of the console's window.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/57570f3b-4a37-4789-bf6c-474fae60171d">Reading Input Buffer Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/a46ba7fd-097a-455d-96ac-13aa01e11dc1">INPUT_RECORD</a>



<a href="https://msdn.microsoft.com/9982dc20-43bd-4ee3-a68d-157c9134daca">PeekConsoleInput</a>



<a href="https://msdn.microsoft.com/5a9f7b18-cdea-4041-a377-5532d30e0105">ReadConsoleInput</a>



<a href="https://msdn.microsoft.com/ad06231f-5063-4aff-b14d-8df5e6e42430">WriteConsoleInput</a>
 

 

