---
UID: NF:winuser.mouse_event
title: mouse_event function (winuser.h)
description: The mouse_event function synthesizes mouse motion and button clicks.
helpviewer_keywords: ["MOUSEEVENTF_ABSOLUTE","MOUSEEVENTF_HWHEEL","MOUSEEVENTF_LEFTDOWN","MOUSEEVENTF_LEFTUP","MOUSEEVENTF_MIDDLEDOWN","MOUSEEVENTF_MIDDLEUP","MOUSEEVENTF_MOVE","MOUSEEVENTF_RIGHTDOWN","MOUSEEVENTF_RIGHTUP","MOUSEEVENTF_WHEEL","MOUSEEVENTF_XDOWN","MOUSEEVENTF_XUP","XBUTTON1","XBUTTON2","_win32_mouse_event","_win32_mouse_event_cpp","inputdev.mouse_event","mouse_event","mouse_event function [Keyboard and Mouse Input]","winui._win32_mouse_event","winuser/mouse_event"]
old-location: inputdev\mouse_event.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\mouse_event.htm
ms.date: 12/05/2018
ms.keywords: MOUSEEVENTF_ABSOLUTE, MOUSEEVENTF_HWHEEL, MOUSEEVENTF_LEFTDOWN, MOUSEEVENTF_LEFTUP, MOUSEEVENTF_MIDDLEDOWN, MOUSEEVENTF_MIDDLEUP, MOUSEEVENTF_MOVE, MOUSEEVENTF_RIGHTDOWN, MOUSEEVENTF_RIGHTUP, MOUSEEVENTF_WHEEL, MOUSEEVENTF_XDOWN, MOUSEEVENTF_XUP, XBUTTON1, XBUTTON2, _win32_mouse_event, _win32_mouse_event_cpp, inputdev.mouse_event, mouse_event, mouse_event function [Keyboard and Mouse Input], winui._win32_mouse_event, winuser/mouse_event
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mouse_event
 - winuser/mouse_event
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - ext-ms-win-ntuser-misc-l1-1-0.dll
 - User32.dll
api_name:
 - mouse_event
---

# mouse_event function


## -description

The <b>mouse_event</b> function synthesizes mouse motion and button clicks.
<div class="alert"><b>Note</b>  This function has been superseded. Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a> instead.</div><div> </div>

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

Controls various aspects of mouse motion and button clicking. This parameter can be certain combinations of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_ABSOLUTE"></a><a id="mouseeventf_absolute"></a><dl>
<dt><b>MOUSEEVENTF_ABSOLUTE</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
The 
						<i>dx</i> and 
						<i>dy</i> parameters contain normalized absolute coordinates. If not set, those parameters contain relative data: the change in position since the last reported position. This flag can be set, or not set, regardless of what kind of mouse or mouse-like device, if any, is connected to the system. For further information about relative mouse motion, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_LEFTDOWN"></a><a id="mouseeventf_leftdown"></a><dl>
<dt><b>MOUSEEVENTF_LEFTDOWN</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The left button is down.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_LEFTUP"></a><a id="mouseeventf_leftup"></a><dl>
<dt><b>MOUSEEVENTF_LEFTUP</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The left button is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_MIDDLEDOWN"></a><a id="mouseeventf_middledown"></a><dl>
<dt><b>MOUSEEVENTF_MIDDLEDOWN</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The middle button is down.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_MIDDLEUP"></a><a id="mouseeventf_middleup"></a><dl>
<dt><b>MOUSEEVENTF_MIDDLEUP</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
The middle button is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_MOVE"></a><a id="mouseeventf_move"></a><dl>
<dt><b>MOUSEEVENTF_MOVE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Movement occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_RIGHTDOWN"></a><a id="mouseeventf_rightdown"></a><dl>
<dt><b>MOUSEEVENTF_RIGHTDOWN</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The right button is down.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_RIGHTUP"></a><a id="mouseeventf_rightup"></a><dl>
<dt><b>MOUSEEVENTF_RIGHTUP</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The right button is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_WHEEL"></a><a id="mouseeventf_wheel"></a><dl>
<dt><b>MOUSEEVENTF_WHEEL</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
The wheel has been moved, if the mouse has a wheel. The amount of movement is specified in 
						<i>dwData</i>

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_XDOWN"></a><a id="mouseeventf_xdown"></a><dl>
<dt><b>MOUSEEVENTF_XDOWN</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
An X button was pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_XUP"></a><a id="mouseeventf_xup"></a><dl>
<dt><b>MOUSEEVENTF_XUP</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
An X button was released.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_WHEEL"></a><a id="mouseeventf_wheel"></a><dl>
<dt><b>MOUSEEVENTF_WHEEL</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
The wheel button is rotated.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_HWHEEL"></a><a id="mouseeventf_hwheel"></a><dl>
<dt><b>MOUSEEVENTF_HWHEEL</b></dt>
<dt>0x01000</dt>
</dl>
</td>
<td width="60%">
The wheel button is tilted.

</td>
</tr>
</table>
 

The values that specify mouse button status are set to indicate changes in status, not ongoing conditions. For example, if the left mouse button is pressed and held down, <b>MOUSEEVENTF_LEFTDOWN</b> is set when the left button is first pressed, but not for subsequent motions. Similarly, <b>MOUSEEVENTF_LEFTUP</b> is set only when the button is first released. 

You cannot specify both <b>MOUSEEVENTF_WHEEL</b> and either <b>MOUSEEVENTF_XDOWN</b> or <b>MOUSEEVENTF_XUP</b> simultaneously in the 
						<i>dwFlags</i> parameter, because they both require use of the 
						<i>dwData</i> field.

### -param dx [in]

Type: <b>DWORD</b>

The mouse's absolute position along the x-axis or its amount of motion since the last mouse event was generated, depending on the setting of <b>MOUSEEVENTF_ABSOLUTE</b>. Absolute data is specified as the mouse's actual x-coordinate; relative data is specified as the number of mickeys moved. A 
					<i>mickey</i> is the amount that a mouse has to move for it to report that it has moved.

### -param dy [in]

Type: <b>DWORD</b>

The mouse's absolute position along the y-axis or its amount of motion since the last mouse event was generated, depending on the setting of <b>MOUSEEVENTF_ABSOLUTE</b>. Absolute data is specified as the mouse's actual y-coordinate; relative data is specified as the number of mickeys moved.

### -param dwData [in]

Type: <b>DWORD</b>

If 
					<i>dwFlags</i> contains <b>MOUSEEVENTF_WHEEL</b>, then 
					<i>dwData</i> specifies the amount of wheel movement. A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. One wheel click is defined as <b>WHEEL_DELTA</b>, which is 120. 

If <i>dwFlags</i> contains <b>MOUSEEVENTF_HWHEEL</b>, then 
					<i>dwData</i> specifies the amount of wheel movement. A positive value indicates that the wheel was tilted to the right; a negative value indicates that the wheel was tilted to the left.

If 
						<i>dwFlags</i> contains <b>MOUSEEVENTF_XDOWN</b> or <b>MOUSEEVENTF_XUP</b>, then 
						<i>dwData</i> specifies which X buttons were pressed or released. This value may be any combination of the following flags. 

If 
						<i>dwFlags</i> is not <b>MOUSEEVENTF_WHEEL</b>, <b>MOUSEEVENTF_XDOWN</b>, or <b>MOUSEEVENTF_XUP</b>, then 
						<i>dwData</i> should be zero. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XBUTTON1"></a><a id="xbutton1"></a><dl>
<dt><b>XBUTTON1</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Set if the first X button was pressed or released.

</td>
</tr>
<tr>
<td width="40%"><a id="XBUTTON2"></a><a id="xbutton2"></a><dl>
<dt><b>XBUTTON2</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Set if the second X button was pressed or released.

</td>
</tr>
</table>

### -param dwExtraInfo [in]

Type: <b>ULONG_PTR</b>

An additional value associated with the mouse event. An application calls <a href="/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> to obtain this extra information.

## -remarks

If the mouse has moved, indicated by <b>MOUSEEVENTF_MOVE</b> being set, 
				<i>dx</i> and 
				<i>dy</i> hold information about that motion. The information is specified as absolute or relative integer values. 

If <b>MOUSEEVENTF_ABSOLUTE</b> value is specified, 
				<i>dx</i> and 
				<i>dy</i> contain normalized absolute coordinates between 0 and 65,535. The event procedure maps these coordinates onto the display surface. Coordinate (0,0) maps onto the upper-left corner of the display surface, (65535,65535) maps onto the lower-right corner. 

If the <b>MOUSEEVENTF_ABSOLUTE</b> value is not specified, 
				<i>dx</i> and 
				<i>dy</i> specify relative motions from when the last mouse event was generated (the last reported position). Positive values mean the mouse moved right (or down); negative values mean the mouse moved left (or up). 

Relative mouse motion is subject to the settings for mouse speed and acceleration level. An end user sets these values using the Mouse application in Control Panel. An application obtains and sets these values with the <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function. 

The system applies two tests to the specified relative mouse motion when applying acceleration. If the specified distance along either the x or y axis is greater than the first mouse threshold value, and the mouse acceleration level is not zero, the operating system doubles the distance. If the specified distance along either the x- or y-axis is greater than the second mouse threshold value, and the mouse acceleration level is equal to two, the operating system doubles the distance that resulted from applying the first threshold test. It is thus possible for the operating system to multiply relatively-specified mouse motion along the x- or y-axis by up to four times.

Once acceleration has been applied, the system scales the resultant value by the desired mouse speed. Mouse speed can range from 1 (slowest) to 20 (fastest) and represents how much the pointer moves based on the distance the mouse moves. The default value is 10, which results in no additional modification to the mouse motion. 

The <b>mouse_event</b> function is used to synthesize mouse events by applications that need to do so. It is also used by applications that need to obtain more information from the mouse than its position and button state. For example, if a tablet manufacturer wants to pass pen-based information to its own applications, it can write a DLL that communicates directly to the tablet hardware, obtains the extra information, and saves it in a queue. The DLL then calls <b>mouse_event</b> with the standard button and x/y position data, along with, in the <i>dwExtraInfo</i> parameter, some pointer or index to the queued extra information. When the application needs the extra information, it calls the DLL with the pointer or index stored in 
				<i>dwExtraInfo</i>, and the DLL returns the extra information.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>