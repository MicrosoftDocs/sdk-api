---
UID: NS:winuser.tagRAWMOUSE
title: RAWMOUSE (winuser.h)
description: Contains information about the state of the mouse.
helpviewer_keywords: ["*LPRAWMOUSE","*PRAWMOUSE","LPRAWMOUSE","LPRAWMOUSE structure pointer [Keyboard and Mouse Input]","MOUSE_ATTRIBUTES_CHANGED","MOUSE_MOVE_ABSOLUTE","MOUSE_MOVE_RELATIVE","MOUSE_VIRTUAL_DESKTOP","PRAWMOUSE","PRAWMOUSE structure pointer [Keyboard and Mouse Input]","RAWMOUSE","RAWMOUSE structure [Keyboard and Mouse Input]","RI_MOUSE_BUTTON_1_DOWN","RI_MOUSE_BUTTON_1_UP","RI_MOUSE_BUTTON_2_DOWN","RI_MOUSE_BUTTON_2_UP","RI_MOUSE_BUTTON_3_DOWN","RI_MOUSE_BUTTON_3_UP","RI_MOUSE_BUTTON_4_DOWN","RI_MOUSE_BUTTON_4_UP","RI_MOUSE_BUTTON_5_DOWN","RI_MOUSE_BUTTON_5_UP","RI_MOUSE_LEFT_BUTTON_DOWN","RI_MOUSE_LEFT_BUTTON_UP","RI_MOUSE_MIDDLE_BUTTON_DOWN","RI_MOUSE_MIDDLE_BUTTON_UP","RI_MOUSE_RIGHT_BUTTON_DOWN","RI_MOUSE_RIGHT_BUTTON_UP","RI_MOUSE_WHEEL","_win32_RAWMOUSE_str","_win32_rawmouse_str_cpp","inputdev.rawmouse","winui._win32_rawmouse_str","winuser/LPRAWMOUSE","winuser/PRAWMOUSE","winuser/RAWMOUSE"]
old-location: inputdev\rawmouse.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawmouse.htm
ms.date: 12/05/2018
ms.keywords: '*LPRAWMOUSE, *PRAWMOUSE, LPRAWMOUSE, LPRAWMOUSE structure pointer [Keyboard and Mouse Input], MOUSE_ATTRIBUTES_CHANGED, MOUSE_MOVE_ABSOLUTE, MOUSE_MOVE_RELATIVE, MOUSE_VIRTUAL_DESKTOP, PRAWMOUSE, PRAWMOUSE structure pointer [Keyboard and Mouse Input], RAWMOUSE, RAWMOUSE structure [Keyboard and Mouse Input], RI_MOUSE_BUTTON_1_DOWN, RI_MOUSE_BUTTON_1_UP, RI_MOUSE_BUTTON_2_DOWN, RI_MOUSE_BUTTON_2_UP, RI_MOUSE_BUTTON_3_DOWN, RI_MOUSE_BUTTON_3_UP, RI_MOUSE_BUTTON_4_DOWN, RI_MOUSE_BUTTON_4_UP, RI_MOUSE_BUTTON_5_DOWN, RI_MOUSE_BUTTON_5_UP, RI_MOUSE_LEFT_BUTTON_DOWN, RI_MOUSE_LEFT_BUTTON_UP, RI_MOUSE_MIDDLE_BUTTON_DOWN, RI_MOUSE_MIDDLE_BUTTON_UP, RI_MOUSE_RIGHT_BUTTON_DOWN, RI_MOUSE_RIGHT_BUTTON_UP, RI_MOUSE_WHEEL, _win32_RAWMOUSE_str, _win32_rawmouse_str_cpp, inputdev.rawmouse, winui._win32_rawmouse_str, winuser/LPRAWMOUSE, winuser/PRAWMOUSE, winuser/RAWMOUSE'
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
targetos: Windows
req.typenames: RAWMOUSE, *PRAWMOUSE, *LPRAWMOUSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRAWMOUSE
 - winuser/tagRAWMOUSE
 - PRAWMOUSE
 - winuser/PRAWMOUSE
 - RAWMOUSE
 - winuser/RAWMOUSE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - tagRAWMOUSE
 - PRAWMOUSE
 - RAWMOUSE
---

# RAWMOUSE structure


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
<td width="40%"><a id="MOUSE_MOVE_RELATIVE"></a><a id="mouse_move_relative"></a><dl>
<dt><b>MOUSE_MOVE_RELATIVE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Mouse movement data is relative to the last mouse position. For further information about mouse motion, see the following Remarks section.
</td>
</tr>
<tr>
<td width="40%"><a id="MOUSE_MOVE_ABSOLUTE"></a><a id="mouse_move_absolute"></a><dl>
<dt><b>MOUSE_MOVE_ABSOLUTE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Mouse movement data is based on absolute position. For further information about mouse motion, see the following Remarks section.
</td>
</tr>
<tr>
<td width="40%"><a id="MOUSE_VIRTUAL_DESKTOP"></a><a id="mouse_virtual_desktop"></a><dl>
<dt><b>MOUSE_VIRTUAL_DESKTOP</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Mouse coordinates are mapped to the virtual desktop (for a multiple monitor system). For further information about mouse motion, see the following Remarks section.
</td>
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
<td width="40%"><a id="MOUSE_MOVE_NOCOALESCE"></a><a id="mouse_move_nocoalesce"></a><dl>
<dt><b>MOUSE_MOVE_NOCOALESCE</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
This mouse movement event was not coalesced. Mouse movement events can be coalescened by default.<br/>
Windows XP/2000:  This value is not supported.
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
Raw input comes from a mouse wheel. The wheel delta is stored in <b>usButtonData</b>.<br/>
A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. For further information see the following Remarks section.
</td>
</tr>
<tr>
<td width="40%"><a id="RI_MOUSE_HWHEEL"></a><a id="ri_mouse_hwheel"></a><dl>
<dt><b>RI_MOUSE_HWHEEL</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Raw input comes from a horizontal mouse wheel. The wheel delta is stored in <b>usButtonData</b>.<br/>
A positive value indicates that the wheel was rotated to the right; a negative value indicates that the wheel was rotated to the left. For further information see the following Remarks section.<br/>
Windows XP/2000:  This value is not supported.
</td>
</tr>
</table>

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.usButtonData

Type: <b>USHORT</b>

If <b>usButtonFlags</b> has <b>RI_MOUSE_WHEEL</b> or <b>RI_MOUSE_HWHEEL</b>, this member specifies the distance the wheel is rotated. For further information see the following Remarks section.

### -field ulRawButtons

Type: <b>ULONG</b>

The raw state of the mouse buttons. The Win32 subsystem does not use this member.

### -field lLastX

Type: <b>LONG</b>

The motion in the X direction. This is signed relative motion or absolute motion, depending on the value of <b>usFlags</b>.

### -field lLastY

Type: <b>LONG</b>

The motion in the Y direction. This is signed relative motion or absolute motion, depending on the value of <b>usFlags</b>.

### -field ulExtraInformation

Type: <b>ULONG</b>

The device-specific additional information for the event.

## -remarks

If the mouse has moved, indicated by <b>MOUSE_MOVE_RELATIVE</b> or <b>MOUSE_MOVE_ABSOLUTE</b>, <b>lLastX</b> and <b>lLastY</b> specify information about that movement. The information is specified as relative or absolute integer values.

If <b>MOUSE_MOVE_RELATIVE</b> value is specified, <b>lLastX</b> and <b>lLastY</b> specify movement relative to the previous mouse event (the last reported position). Positive values mean the mouse moved right (or down); negative values mean the mouse moved left (or up).

If <b>MOUSE_MOVE_ABSOLUTE</b> value is specified, <b>lLastX</b> and <b>lLastY</b> contain normalized absolute coordinates between 0 and 65,535. Coordinate (0,0) maps onto the upper-left corner of the display surface; coordinate (65535,65535) maps onto the lower-right corner. In a multimonitor system, the coordinates map to the primary monitor.

If <b>MOUSE_VIRTUAL_DESKTOP</b> is specified in addition to <b>MOUSE_MOVE_ABSOLUTE</b>, the coordinates map to the entire virtual desktop.

```cpp
if ((rawMouse.usFlags & MOUSE_MOVE_ABSOLUTE) == MOUSE_MOVE_ABSOLUTE)
{
    bool isVirtualDesktop = (rawMouse.usFlags & MOUSE_VIRTUAL_DESKTOP) == MOUSE_VIRTUAL_DESKTOP;

    int width = GetSystemMetrics(isVirtualDesktop ? SM_CXVIRTUALSCREEN : SM_CXSCREEN);
    int height = GetSystemMetrics(isVirtualDesktop ? SM_CYVIRTUALSCREEN : SM_CYSCREEN);

    int absoluteX = int((rawMouse.lLastX / 65535.0f) * width);
    int absoluteY = int((rawMouse.lLastY / 65535.0f) * height);
}
else if (rawMouse.lLastX != 0 || rawMouse.lLastY != 0)
{
    int relativeX = rawMouse.lLastX;
    int relativeY = rawMouse.lLastY;
}
```

In contrast to legacy [WM_MOUSEMOVE](/windows/win32/inputdev/wm-mousemove) window messages Raw Input mouse events is not subject to the effects of the mouse speed set in the Control Panel's <b>Mouse Properties</b> sheet. See [About Mouse Input](/windows/win32/inputdev/about-mouse-input) for details.

If mouse wheel is moved, indicated by <b>RI_MOUSE_WHEEL</b> or <b>RI_MOUSE_HWHEEL</b> in <b>usButtonFlags</b>, then <b>usButtonData</b> contains a signed <b>short</b> value that specifies the distance the wheel is rotated.

The wheel rotation will be a multiple of <b>WHEEL_DELTA</b>, which is set at 120. This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.

The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message. To use this feature, you can either add the incoming delta values until <b>WHEEL_DELTA</b> is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to the more frequent messages. You can also choose your scroll granularity and accumulate deltas until it is reached.

The application could also retrieve the current lines-to-scroll and characters-to-scroll user setting by using the [SystemParametersInfo](nf-winuser-systemparametersinfoa.md) API with <b>SPI_GETWHEELSCROLLLINES</b> or <b>SPI_GETWHEELSCROLLCHARS</b> parameter.

Here is example of such wheel handling code:

```cpp
if ((rawMouse.usButtonFlags & RI_MOUSE_WHEEL) == RI_MOUSE_WHEEL ||
    (rawMouse.usButtonFlags & RI_MOUSE_HWHEEL) == RI_MOUSE_HWHEEL)
{
    static const unsigned long defaultScrollLinesPerWheelDelta = 3;
    static const unsigned long defaultScrollCharsPerWheelDelta = 1;

    float wheelDelta = (float)(short)rawMouse.usButtonData;
    float numTicks = wheelDelta / WHEEL_DELTA;

    bool isHorizontalScroll = (rawMouse.usButtonFlags & RI_MOUSE_HWHEEL) == RI_MOUSE_HWHEEL;
    bool isScrollByPage = false;
    float scrollDelta = numTicks;

    if (isHorizontalScroll)
    {
        unsigned long scrollChars = defaultScrollCharsPerWheelDelta;
        SystemParametersInfo(SPI_GETWHEELSCROLLCHARS, 0, &scrollChars, 0);
        scrollDelta *= scrollChars;
    }
    else
    {
        unsigned long scrollLines = defaultScrollLinesPerWheelDelta;
        SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, &scrollLines, 0);
        if (scrollLines == WHEEL_PAGESCROLL)
            isScrollByPage = true;
        else
            scrollDelta *= scrollLines;
    }
}
```

## -see-also

<b>Conceptual</b>

[GetRawInputDeviceInfo](nf-winuser-getrawinputdeviceinfoa.md)

[RAWINPUT](ns-winuser-rawinput.md)

[Raw Input](/windows/win32/inputdev/raw-input)

<b>Reference</b>

[MOUSEINPUT structure](ns-winuser-mouseinput.md)

[SendInput function](nf-winuser-sendinput.md)

[MOUSE_INPUT_DATA structure](../ntddmou/ns-ntddmou-mouse_input_data.md)

[About Mouse Input (legacy)](/windows/win32/inputdev/about-mouse-input)

[Mouse Input Notifications (legacy)](/windows/win32/inputdev/mouse-input-notifications)

[SystemParametersInfo](nf-winuser-systemparametersinfoa.md)

