---
UID: NS:winuser.tagRAWMOUSE
title: tagRAWMOUSE
author: windows-sdk-content
description: Contains information about the state of the mouse.
old-location: inputdev\rawmouse.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawmouse.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPRAWMOUSE, *PRAWMOUSE, LPRAWMOUSE, LPRAWMOUSE structure pointer [Keyboard and Mouse Input], MOUSE_ATTRIBUTES_CHANGED, MOUSE_MOVE_ABSOLUTE, MOUSE_MOVE_RELATIVE, MOUSE_VIRTUAL_DESKTOP, PRAWMOUSE, PRAWMOUSE structure pointer [Keyboard and Mouse Input], RAWMOUSE, RAWMOUSE structure [Keyboard and Mouse Input], RI_MOUSE_BUTTON_1_DOWN, RI_MOUSE_BUTTON_1_UP, RI_MOUSE_BUTTON_2_DOWN, RI_MOUSE_BUTTON_2_UP, RI_MOUSE_BUTTON_3_DOWN, RI_MOUSE_BUTTON_3_UP, RI_MOUSE_BUTTON_4_DOWN, RI_MOUSE_BUTTON_4_UP, RI_MOUSE_BUTTON_5_DOWN, RI_MOUSE_BUTTON_5_UP, RI_MOUSE_LEFT_BUTTON_DOWN, RI_MOUSE_LEFT_BUTTON_UP, RI_MOUSE_MIDDLE_BUTTON_DOWN, RI_MOUSE_MIDDLE_BUTTON_UP, RI_MOUSE_RIGHT_BUTTON_DOWN, RI_MOUSE_RIGHT_BUTTON_UP, RI_MOUSE_WHEEL, _win32_RAWMOUSE_str, _win32_rawmouse_str_cpp, inputdev.rawmouse, tagRAWMOUSE, winui._win32_rawmouse_str, winuser/LPRAWMOUSE, winuser/PRAWMOUSE, winuser/RAWMOUSE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - RAWMOUSE
product: Windows
targetos: Windows
req.typenames: RAWMOUSE, *PRAWMOUSE, *LPRAWMOUSE
req.redist: 
---

# tagRAWMOUSE structure


## -description


Contains information about the state of the mouse. 


## -struct-fields




### -field usFlags

Type: <b>USHORT</b>

The mouse state. This member can be any reasonable combination of the following. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MOUSE_ATTRIBUTES_CHANGED"></a><a id="mouse_attributes_changed"></a><dl>
<dt><b>MOUSE_ATTRIBUTES_CHANGED</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Mouse attributes changed; application needs to query the mouse attributes.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSE_MOVE_RELATIVE"></a><a id="mouse_move_relative"></a><dl>
<dt><b>MOUSE_MOVE_RELATIVE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Mouse movement data is relative to the last mouse position.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSE_MOVE_ABSOLUTE"></a><a id="mouse_move_absolute"></a><dl>
<dt><b>MOUSE_MOVE_ABSOLUTE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Mouse movement data is based on absolute position.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSE_VIRTUAL_DESKTOP"></a><a id="mouse_virtual_desktop"></a><dl>
<dt><b>MOUSE_VIRTUAL_DESKTOP</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Mouse coordinates are mapped to the virtual desktop (for a multiple monitor system).

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.ulButtons

Type: <b>ULONG</b>

Reserved.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.usButtonFlags

Type: <b>USHORT</b>

The transition state of the mouse buttons. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_LEFT_BUTTON_DOWN"></a><a id="ri_mouse_left_button_down"></a><dl>
<dt><b>RI_MOUSE_LEFT_BUTTON_DOWN</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Left button changed to down.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_LEFT_BUTTON_UP"></a><a id="ri_mouse_left_button_up"></a><dl>
<dt><b>RI_MOUSE_LEFT_BUTTON_UP</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Left button changed to up.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_MIDDLE_BUTTON_DOWN"></a><a id="ri_mouse_middle_button_down"></a><dl>
<dt><b>RI_MOUSE_MIDDLE_BUTTON_DOWN</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Middle button changed to down.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_MIDDLE_BUTTON_UP"></a><a id="ri_mouse_middle_button_up"></a><dl>
<dt><b>RI_MOUSE_MIDDLE_BUTTON_UP</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Middle button changed to up.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_RIGHT_BUTTON_DOWN"></a><a id="ri_mouse_right_button_down"></a><dl>
<dt><b>RI_MOUSE_RIGHT_BUTTON_DOWN</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Right button changed to down.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_RIGHT_BUTTON_UP"></a><a id="ri_mouse_right_button_up"></a><dl>
<dt><b>RI_MOUSE_RIGHT_BUTTON_UP</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Right button changed to up.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_1_DOWN"></a><a id="ri_mouse_button_1_down"></a><dl>
<dt><b>RI_MOUSE_BUTTON_1_DOWN</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
RI_MOUSE_LEFT_BUTTON_DOWN

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_1_UP"></a><a id="ri_mouse_button_1_up"></a><dl>
<dt><b>RI_MOUSE_BUTTON_1_UP</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
RI_MOUSE_LEFT_BUTTON_UP

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_2_DOWN"></a><a id="ri_mouse_button_2_down"></a><dl>
<dt><b>RI_MOUSE_BUTTON_2_DOWN</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
RI_MOUSE_RIGHT_BUTTON_DOWN

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_2_UP"></a><a id="ri_mouse_button_2_up"></a><dl>
<dt><b>RI_MOUSE_BUTTON_2_UP</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
RI_MOUSE_RIGHT_BUTTON_UP

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_3_DOWN"></a><a id="ri_mouse_button_3_down"></a><dl>
<dt><b>RI_MOUSE_BUTTON_3_DOWN</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
RI_MOUSE_MIDDLE_BUTTON_DOWN

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_3_UP"></a><a id="ri_mouse_button_3_up"></a><dl>
<dt><b>RI_MOUSE_BUTTON_3_UP</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
RI_MOUSE_MIDDLE_BUTTON_UP

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_4_DOWN"></a><a id="ri_mouse_button_4_down"></a><dl>
<dt><b>RI_MOUSE_BUTTON_4_DOWN</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
XBUTTON1 changed to down.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_4_UP"></a><a id="ri_mouse_button_4_up"></a><dl>
<dt><b>RI_MOUSE_BUTTON_4_UP</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
XBUTTON1 changed to up.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_5_DOWN"></a><a id="ri_mouse_button_5_down"></a><dl>
<dt><b>RI_MOUSE_BUTTON_5_DOWN</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
XBUTTON2 changed to down.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_BUTTON_5_UP"></a><a id="ri_mouse_button_5_up"></a><dl>
<dt><b>RI_MOUSE_BUTTON_5_UP</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
XBUTTON2 changed to up.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_WHEEL"></a><a id="ri_mouse_wheel"></a><dl>
<dt><b>RI_MOUSE_WHEEL</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Raw input comes from a mouse wheel. The wheel delta is stored in <b>usButtonData</b>.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.usButtonData

Type: <b>USHORT</b>

If <b>usButtonFlags</b> is <b>RI_MOUSE_WHEEL</b>, this member is a signed value that specifies the wheel delta. 


### -field ulRawButtons

Type: <b>ULONG</b>

The raw state of the mouse buttons. 


### -field lLastX

Type: <b>LONG</b>

The motion in the X direction. This is signed relative motion or absolute motion, depending on the value of <b>usFlags</b>. 


### -field lLastY

Type: <b>LONG</b>

The motion in the Y direction. This is signed relative motion or absolute motion, depending on the value of <b>usFlags</b>. 


### -field ulExtraInformation

Type: <b>ULONG</b>

The device-specific additional information for the event. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645597(v=VS.85).aspx">GetRawInputDeviceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645562(v=VS.85).aspx">RAWINPUT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645536(v=VS.85).aspx">Raw Input</a>



<b>Reference</b>
 

 

