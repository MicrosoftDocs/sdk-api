---
UID: NS:winuser.tagMOUSEINPUT
title: tagMOUSEINPUT
author: windows-sdk-content
description: Contains information about a simulated mouse event.
old-location: inputdev\mouseinput.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputstructures\mouseinput.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPMOUSEINPUT, *PMOUSEINPUT, MOUSEEVENTF_ABSOLUTE, MOUSEEVENTF_HWHEEL, MOUSEEVENTF_LEFTDOWN, MOUSEEVENTF_LEFTUP, MOUSEEVENTF_MIDDLEDOWN, MOUSEEVENTF_MIDDLEUP, MOUSEEVENTF_MOVE, MOUSEEVENTF_MOVE_NOCOALESCE, MOUSEEVENTF_RIGHTDOWN, MOUSEEVENTF_RIGHTUP, MOUSEEVENTF_VIRTUALDESK, MOUSEEVENTF_WHEEL, MOUSEEVENTF_XDOWN, MOUSEEVENTF_XUP, MOUSEINPUT, MOUSEINPUT structure [Keyboard and Mouse Input], PMOUSEINPUT, PMOUSEINPUT structure pointer [Keyboard and Mouse Input], XBUTTON1, XBUTTON2, _win32_MOUSEINPUT_str, _win32_mouseinput_str_cpp, inputdev.mouseinput, tagMOUSEINPUT, winui._win32_mouseinput_str, winuser/MOUSEINPUT, winuser/PMOUSEINPUT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: MOUSEINPUT, *PMOUSEINPUT, *LPMOUSEINPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MOUSEINPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagMOUSEINPUT structure


## -description


Contains information about a simulated mouse event.


## -struct-fields




### -field dx

Type: <b>LONG</b>

The absolute position of the mouse, or the amount of motion since the last mouse event was generated, depending on the value of the <b>dwFlags</b> member. Absolute data is specified as the x coordinate of the mouse; relative data is specified as the number of pixels moved. 


### -field dy

Type: <b>LONG</b>

The absolute position of the mouse, or the amount of motion since the last mouse event was generated, depending on the value of the <b>dwFlags</b> member. Absolute data is specified as the y coordinate of the mouse; relative data is specified as the number of pixels moved. 


### -field mouseData

Type: <b>DWORD</b>

If <b>dwFlags</b> contains <b>MOUSEEVENTF_WHEEL</b>, then <b>mouseData</b> specifies the amount of wheel movement. A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. One wheel click is defined as <b>WHEEL_DELTA</b>, which is 120.

Windows Vista: If <i>dwFlags</i> contains <b>MOUSEEVENTF_HWHEEL</b>, then 
			  <i>dwData</i> specifies the amount of wheel movement. A positive value indicates that the wheel was rotated to the right; a negative value indicates that the wheel was rotated to the left. One wheel click is defined as <b>WHEEL_DELTA</b>, which is 120.

 If <b>dwFlags</b> does not contain <b>MOUSEEVENTF_WHEEL</b>, <b>MOUSEEVENTF_XDOWN</b>, or <b>MOUSEEVENTF_XUP</b>, then <b>mouseData</b> should be zero. 

If <b>dwFlags</b> contains <b>MOUSEEVENTF_XDOWN</b> or <b>MOUSEEVENTF_XUP</b>, then <b>mouseData</b> specifies which X buttons were pressed or released. This value may be any combination of the following flags. 

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
Set if the first X button is pressed or released.

</td>
</tr>
<tr>
<td width="40%"><a id="XBUTTON2"></a><a id="xbutton2"></a><dl>
<dt><b>XBUTTON2</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Set if the second X button is pressed or released.

</td>
</tr>
</table>
 


### -field dwFlags

Type: <b>DWORD</b>

A set of bit flags that specify various aspects of mouse motion and button clicks. The bits in this member can be any reasonable combination of the following values.

The bit flags that specify mouse button status are set to indicate changes in status, not ongoing conditions. For example, if the left mouse button is pressed and held down, <b>MOUSEEVENTF_LEFTDOWN</b> is set when the left button is first pressed, but not for subsequent motions. Similarly, <b>MOUSEEVENTF_LEFTUP</b> is set only when the button is first released. 

You cannot specify both the <b>MOUSEEVENTF_WHEEL</b> flag and either <b>MOUSEEVENTF_XDOWN</b> or <b>MOUSEEVENTF_XUP</b> flags simultaneously in the <b>dwFlags</b> parameter, because they both require use of the <b>mouseData</b> field. 

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
The <b>dx</b> and <b>dy</b> members contain normalized absolute coordinates. If the flag is not set, <b>dx</b>and <b>dy</b> contain relative data (the change in position since the last reported position). This flag can be set, or not set, regardless of what kind of mouse or other pointing device, if any, is connected to the system. For further information about relative mouse motion, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_HWHEEL"></a><a id="mouseeventf_hwheel"></a><dl>
<dt><b>MOUSEEVENTF_HWHEEL</b></dt>
<dt>0x01000</dt>
</dl>
</td>
<td width="60%">
 The wheel was moved horizontally, if the mouse has a wheel. The amount of movement is specified in <b>mouseData</b>.
					

<b>Windows XP/2000:  </b>This value is not supported.

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
<td width="40%"><a id="MOUSEEVENTF_MOVE_NOCOALESCE"></a><a id="mouseeventf_move_nocoalesce"></a><dl>
<dt><b>MOUSEEVENTF_MOVE_NOCOALESCE</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/en-us/library/ms645616(v=VS.85).aspx">WM_MOUSEMOVE</a> messages will not be coalesced. The default behavior is to coalesce <b>WM_MOUSEMOVE</b> messages.
					

<b>Windows XP/2000:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_LEFTDOWN"></a><a id="mouseeventf_leftdown"></a><dl>
<dt><b>MOUSEEVENTF_LEFTDOWN</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The left button was pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_LEFTUP"></a><a id="mouseeventf_leftup"></a><dl>
<dt><b>MOUSEEVENTF_LEFTUP</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The left button was released.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_RIGHTDOWN"></a><a id="mouseeventf_rightdown"></a><dl>
<dt><b>MOUSEEVENTF_RIGHTDOWN</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The right button was pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_RIGHTUP"></a><a id="mouseeventf_rightup"></a><dl>
<dt><b>MOUSEEVENTF_RIGHTUP</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The right button was released.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_MIDDLEDOWN"></a><a id="mouseeventf_middledown"></a><dl>
<dt><b>MOUSEEVENTF_MIDDLEDOWN</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The middle button was pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_MIDDLEUP"></a><a id="mouseeventf_middleup"></a><dl>
<dt><b>MOUSEEVENTF_MIDDLEUP</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
The middle button was released.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_VIRTUALDESK"></a><a id="mouseeventf_virtualdesk"></a><dl>
<dt><b>MOUSEEVENTF_VIRTUALDESK</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
Maps coordinates to the entire desktop. Must be used with <b>MOUSEEVENTF_ABSOLUTE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSEEVENTF_WHEEL"></a><a id="mouseeventf_wheel"></a><dl>
<dt><b>MOUSEEVENTF_WHEEL</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
 The wheel was moved, if the mouse has a wheel. The amount of movement is specified in <b>mouseData</b>.
					

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
</table>
 


### -field time

Type: <b>DWORD</b>

The time stamp for the event, in milliseconds. If this parameter is 0, the system will provide its own time stamp. 


### -field dwExtraInfo

Type: <b>ULONG_PTR</b>

An additional value associated with the mouse event. An application calls <a href="https://msdn.microsoft.com/en-us/library/ms644937(v=VS.85).aspx">GetMessageExtraInfo</a> to obtain this extra information. 


## -remarks



If the mouse has moved, indicated by <b>MOUSEEVENTF_MOVE</b>, <b>dx</b>and <b>dy</b> specify information about that movement. The information is specified as absolute or relative integer values. 

If <b>MOUSEEVENTF_ABSOLUTE</b> value is specified, <b>dx</b> and <b>dy</b> contain normalized absolute coordinates between 0 and 65,535. The event procedure maps these coordinates onto the display surface. Coordinate (0,0) maps onto the upper-left corner of the display surface; coordinate (65535,65535) maps onto the lower-right corner. In a multimonitor system, the coordinates map to the primary monitor. 

 If <b>MOUSEEVENTF_VIRTUALDESK</b> is specified, the coordinates map to the entire virtual desktop.

If the <b>MOUSEEVENTF_ABSOLUTE</b> value is not specified, <b>dx</b>and <b>dy</b> specify movement relative to the previous mouse event (the last reported position). Positive values mean the mouse moved right (or down); negative values mean the mouse moved left (or up). 

Relative mouse motion is subject to the effects of the mouse speed and the two-mouse threshold values. A user sets these three values with the <b>Pointer Speed</b> slider of the Control Panel's <b>Mouse Properties</b> sheet. You can obtain and set these values using the <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function. 

The system applies two tests to the specified relative mouse movement. If the specified distance along either the x or y axis is greater than the first mouse threshold value, and the mouse speed is not zero, the system doubles the distance. If the specified distance along either the x or y axis is greater than the second mouse threshold value, and the mouse speed is equal to two, the system doubles the distance that resulted from applying the first threshold test. It is thus possible for the system to multiply specified relative mouse movement along the x or y axis by up to four times.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644937(v=VS.85).aspx">GetMessageExtraInfo</a>



<a href="https://msdn.microsoft.com/733638f6-e9a0-497d-af70-3b70c8c1193c">INPUT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646310(v=VS.85).aspx">SendInput</a>
 

 

