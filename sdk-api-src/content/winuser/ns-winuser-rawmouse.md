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
 - RAWMOUSE
---

# RAWMOUSE structure

## -description

Contains information about the state of the mouse.

## -struct-fields

### -field usFlags

Type: **USHORT**

The mouse state. This member can be any reasonable combination of the following. 

| Value | Meaning |
|-------|---------|
| **MOUSE_MOVE_RELATIVE**</br>0x00 | Mouse movement data is relative to the last mouse position. For further information about mouse motion, see the following Remarks section. |
| **MOUSE_MOVE_ABSOLUTE**</br>0x01 | Mouse movement data is based on absolute position. For further information about mouse motion, see the following Remarks section. |
| **MOUSE_VIRTUAL_DESKTOP**</br>0x02 | Mouse coordinates are mapped to the virtual desktop (for a multiple monitor system). For further information about mouse motion, see the following Remarks section. |
| **MOUSE_ATTRIBUTES_CHANGED**</br>0x04 | Mouse attributes changed; application needs to query the mouse attributes. |
| **MOUSE_MOVE_NOCOALESCE**</br>0x08 | This mouse movement event was not coalesced. Mouse movement events can be coalesced by default.<br/>Windows XP/2000: This value is not supported. |

### -field DUMMYUNIONNAME.ulButtons

Type: **ULONG**

Reserved.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.usButtonFlags

Type: **USHORT**

The transition state of the mouse buttons. This member can be one or more of the following values. 

| Value | Meaning |
|-------|---------|
| **RI_MOUSE_BUTTON_1_DOWN**</br>**RI_MOUSE_LEFT_BUTTON_DOWN**</br>0x0001 | Left button changed to down. |
| **RI_MOUSE_BUTTON_1_UP**</br>**RI_MOUSE_LEFT_BUTTON_UP**</br>0x0002 | Left button changed to up. |
| **RI_MOUSE_BUTTON_2_DOWN**</br>**RI_MOUSE_RIGHT_BUTTON_DOWN**</br>0x0004 | Right button changed to down. |
| **RI_MOUSE_BUTTON_2_UP**</br>**RI_MOUSE_RIGHT_BUTTON_UP**</br>0x0008 | Right button changed to up. |
| **RI_MOUSE_BUTTON_3_DOWN**</br>**RI_MOUSE_MIDDLE_BUTTON_DOWN**</br>0x0010 | Middle button changed to down. |
| **RI_MOUSE_BUTTON_3_UP**</br>**RI_MOUSE_MIDDLE_BUTTON_UP**</br>0x0020 | Middle button changed to up. |
| **RI_MOUSE_BUTTON_4_DOWN**</br>0x0040 | XBUTTON1 changed to down. |
| **RI_MOUSE_BUTTON_4_UP**</br>0x0080 | XBUTTON1 changed to up. |
| **RI_MOUSE_BUTTON_5_DOWN**</br>0x0100 | XBUTTON2 changed to down. |
| **RI_MOUSE_BUTTON_5_UP**</br>0x0200 | XBUTTON2 changed to up. |
| **RI_MOUSE_WHEEL**</br>0x0400 | Raw input comes from a mouse wheel. The wheel delta is stored in **usButtonData**.<br/>A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. For further information see the following Remarks section. |
| **RI_MOUSE_HWHEEL**</br>0x0800 | Raw input comes from a horizontal mouse wheel. The wheel delta is stored in **usButtonData**.<br/>A positive value indicates that the wheel was rotated to the right; a negative value indicates that the wheel was rotated to the left. For further information see the following Remarks section.<br/>Windows XP/2000:  This value is not supported. |

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.usButtonData

Type: **USHORT**

If **usButtonFlags** has **RI_MOUSE_WHEEL** or **RI_MOUSE_HWHEEL**, this member specifies the distance the wheel is rotated. For further information see the following Remarks section.

### -field ulRawButtons

Type: **ULONG**

The raw state of the mouse buttons. The Win32 subsystem does not use this member.

### -field lLastX

Type: **LONG**

The motion in the X direction. This is signed relative motion or absolute motion, depending on the value of **usFlags**.

### -field lLastY

Type: **LONG**

The motion in the Y direction. This is signed relative motion or absolute motion, depending on the value of **usFlags**.

### -field ulExtraInformation

Type: **ULONG**

Additional device-specific information for the event. See [Distinguishing Pen Input from Mouse and Touch](/windows/win32/tablet/system-events-and-mouse-messages#distinguishing-pen-input-from-mouse-and-touch) for more info.

## -remarks

If the mouse has moved, indicated by **MOUSE_MOVE_RELATIVE** or **MOUSE_MOVE_ABSOLUTE**, **lLastX** and **lLastY** specify information about that movement. The information is specified as relative or absolute integer values.

If **MOUSE_MOVE_RELATIVE** value is specified, **lLastX** and **lLastY** specify movement relative to the previous mouse event (the last reported position). Positive values mean the mouse moved right (or down); negative values mean the mouse moved left (or up).

If **MOUSE_MOVE_ABSOLUTE** value is specified, **lLastX** and **lLastY** contain normalized absolute coordinates between 0 and 65,535. Coordinate (0,0) maps onto the upper-left corner of the display surface; coordinate (65535,65535) maps onto the lower-right corner. In a multimonitor system, the coordinates map to the primary monitor.

If **MOUSE_VIRTUAL_DESKTOP** is specified in addition to **MOUSE_MOVE_ABSOLUTE**, the coordinates map to the entire virtual desktop.

```cpp
case WM_INPUT:
{
    UINT dwSize = sizeof(RAWINPUT);
    static BYTE lpb[sizeof(RAWINPUT)];

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER));

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEMOUSE)
    {
        RAWMOUSE& mouse = raw->data.mouse;

        if (mouse.usFlags & MOUSE_MOVE_ABSOLUTE)
        {
            RECT rect;
            if (mouse.usFlags & MOUSE_VIRTUAL_DESKTOP)
            {
                rect.left = GetSystemMetrics(SM_XVIRTUALSCREEN);
                rect.top = GetSystemMetrics(SM_YVIRTUALSCREEN);
                rect.right = GetSystemMetrics(SM_CXVIRTUALSCREEN);
                rect.bottom = GetSystemMetrics(SM_CYVIRTUALSCREEN);
            }
            else
            {
                rect.left = 0;
                rect.top = 0;
                rect.right = GetSystemMetrics(SM_CXSCREEN);
                rect.bottom = GetSystemMetrics(SM_CYSCREEN);
            }

            int absoluteX = MulDiv(mouse.lLastX, rect.right, USHRT_MAX) + rect.left;
            int absoluteY = MulDiv(mouse.lLastY, rect.bottom, USHRT_MAX) + rect.top;
            ...
        }
        else if (mouse.lLastX != 0 || mouse.lLastY != 0)
        {
            int relativeX = mouse.lLastX;
            int relativeY = mouse.lLastY;
            ...
        }
        ...
    }

    return 0;
}
```

In contrast to legacy [WM_MOUSEMOVE](/windows/win32/inputdev/wm-mousemove) window messages Raw Input mouse events is not subject to the effects of the mouse speed set in the Control Panel's **Mouse Properties** sheet. See [Mouse Input Overview](/windows/win32/inputdev/about-mouse-input) for details.

If mouse wheel is moved, indicated by **RI_MOUSE_WHEEL** or **RI_MOUSE_HWHEEL** in **usButtonFlags**, then **usButtonData** contains a signed **short** value that specifies the distance the wheel is rotated.

The wheel rotation will be a multiple of **WHEEL_DELTA**, which is set at 120. This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.

The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message. To use this feature, you can either add the incoming delta values until **WHEEL_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to the more frequent messages. You can also choose your scroll granularity and accumulate deltas until it is reached.

The application could also retrieve the current lines-to-scroll and characters-to-scroll user setting by using the [SystemParametersInfo](nf-winuser-systemparametersinfoa.md) API with **SPI_GETWHEELSCROLLLINES** or **SPI_GETWHEELSCROLLCHARS** parameter.

Here is example of such wheel handling code:

```cpp
RAWMOUSE& mouse = raw->data.mouse;

if ((mouse.usButtonFlags & RI_MOUSE_WHEEL) || (mouse.usButtonFlags & RI_MOUSE_HWHEEL))
{
    short wheelDelta = (short)mouse.usButtonData;
    float scrollDelta = (float)wheelDelta / WHEEL_DELTA;

    if (mouse.usButtonFlags & RI_MOUSE_HWHEEL) // Horizontal
    {
        unsigned long scrollChars = 1; // 1 is the default
        SystemParametersInfo(SPI_GETWHEELSCROLLCHARS, 0, &scrollChars, 0);
        scrollDelta *= scrollChars;
        ...
    }
    else // Vertical
    {
        unsigned long scrollLines = 3; // 3 is the default
        SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, &scrollLines, 0);
        if (scrollLines != WHEEL_PAGESCROLL)
            scrollDelta *= scrollLines;
        ...
    }
}
```

## -see-also

**Conceptual**

[GetRawInputDeviceInfo](nf-winuser-getrawinputdeviceinfoa.md)

[RAWINPUT](ns-winuser-rawinput.md)

[Raw Input](/windows/win32/inputdev/raw-input)

**Reference**

[MOUSEINPUT structure](ns-winuser-mouseinput.md)

[SendInput function](nf-winuser-sendinput.md)

[MOUSE_INPUT_DATA structure](../ntddmou/ns-ntddmou-mouse_input_data.md)

[Mouse Input Overview (legacy)](/windows/win32/inputdev/about-mouse-input)

[Mouse Input Notifications (legacy)](/windows/win32/inputdev/mouse-input-notifications)

[SystemParametersInfo](nf-winuser-systemparametersinfoa.md)
