---
UID: NS:winuser.tagMOUSEINPUT
title: MOUSEINPUT (winuser.h)
description: Contains information about a simulated mouse event.
helpviewer_keywords: ["*LPMOUSEINPUT","*PMOUSEINPUT","MOUSEEVENTF_ABSOLUTE","MOUSEEVENTF_HWHEEL","MOUSEEVENTF_LEFTDOWN","MOUSEEVENTF_LEFTUP","MOUSEEVENTF_MIDDLEDOWN","MOUSEEVENTF_MIDDLEUP","MOUSEEVENTF_MOVE","MOUSEEVENTF_MOVE_NOCOALESCE","MOUSEEVENTF_RIGHTDOWN","MOUSEEVENTF_RIGHTUP","MOUSEEVENTF_VIRTUALDESK","MOUSEEVENTF_WHEEL","MOUSEEVENTF_XDOWN","MOUSEEVENTF_XUP","MOUSEINPUT","MOUSEINPUT structure [Keyboard and Mouse Input]","PMOUSEINPUT","PMOUSEINPUT structure pointer [Keyboard and Mouse Input]","XBUTTON1","XBUTTON2","_win32_MOUSEINPUT_str","_win32_mouseinput_str_cpp","inputdev.mouseinput","winui._win32_mouseinput_str","winuser/MOUSEINPUT","winuser/PMOUSEINPUT"]
old-location: inputdev\mouseinput.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputstructures\mouseinput.htm
ms.date: 12/05/2018
ms.keywords: '*LPMOUSEINPUT, *PMOUSEINPUT, MOUSEEVENTF_ABSOLUTE, MOUSEEVENTF_HWHEEL, MOUSEEVENTF_LEFTDOWN, MOUSEEVENTF_LEFTUP, MOUSEEVENTF_MIDDLEDOWN, MOUSEEVENTF_MIDDLEUP, MOUSEEVENTF_MOVE, MOUSEEVENTF_MOVE_NOCOALESCE, MOUSEEVENTF_RIGHTDOWN, MOUSEEVENTF_RIGHTUP, MOUSEEVENTF_VIRTUALDESK, MOUSEEVENTF_WHEEL, MOUSEEVENTF_XDOWN, MOUSEEVENTF_XUP, MOUSEINPUT, MOUSEINPUT structure [Keyboard and Mouse Input], PMOUSEINPUT, PMOUSEINPUT structure pointer [Keyboard and Mouse Input], XBUTTON1, XBUTTON2, _win32_MOUSEINPUT_str, _win32_mouseinput_str_cpp, inputdev.mouseinput, winui._win32_mouseinput_str, winuser/MOUSEINPUT, winuser/PMOUSEINPUT'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MOUSEINPUT, *PMOUSEINPUT, *LPMOUSEINPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMOUSEINPUT
 - winuser/tagMOUSEINPUT
 - PMOUSEINPUT
 - winuser/PMOUSEINPUT
 - MOUSEINPUT
 - winuser/MOUSEINPUT
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
 - MOUSEINPUT
---

# MOUSEINPUT structure

## -description

Contains information about a simulated mouse event.

## -struct-fields

### -field dx

Type: **LONG**

The absolute position of the mouse, or the amount of motion since the last mouse event was generated, depending on the value of the **dwFlags** member. Absolute data is specified as the x coordinate of the mouse; relative data is specified as the number of pixels moved.

### -field dy

Type: **LONG**

The absolute position of the mouse, or the amount of motion since the last mouse event was generated, depending on the value of the **dwFlags** member. Absolute data is specified as the y coordinate of the mouse; relative data is specified as the number of pixels moved.

### -field mouseData

Type: **DWORD**

If **dwFlags** contains **MOUSEEVENTF_WHEEL**, then **mouseData** specifies the amount of wheel movement. A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. One wheel click is defined as **WHEEL_DELTA**, which is 120.

**Windows Vista**: If *dwFlags* contains **MOUSEEVENTF_HWHEEL**, then *dwData* specifies the amount of wheel movement. A positive value indicates that the wheel was rotated to the right; a negative value indicates that the wheel was rotated to the left. One wheel click is defined as **WHEEL_DELTA**, which is 120.

 If **dwFlags** does not contain **MOUSEEVENTF_WHEEL**, **MOUSEEVENTF_XDOWN**, or **MOUSEEVENTF_XUP**, then **mouseData** should be zero.

If **dwFlags** contains **MOUSEEVENTF_XDOWN** or **MOUSEEVENTF_XUP**, then **mouseData** specifies which X buttons were pressed or released. This value may be any combination of the following flags.

| Value | Meaning |
|-|-|
| **XBUTTON1**<br>0x0001 | Set if the first X button is pressed or released. |
| **XBUTTON2**<br>0x0002 | Set if the second X button is pressed or released. |

### -field dwFlags

Type: **DWORD**

A set of bit flags that specify various aspects of mouse motion and button clicks. The bits in this member can be any reasonable combination of the following values.

The bit flags that specify mouse button status are set to indicate changes in status, not ongoing conditions. For example, if the left mouse button is pressed and held down, **MOUSEEVENTF_LEFTDOWN** is set when the left button is first pressed, but not for subsequent motions. Similarly **MOUSEEVENTF_LEFTUP** is set only when the button is first released. 

You cannot specify both the **MOUSEEVENTF_WHEEL** flag and either **MOUSEEVENTF_XDOWN** or **MOUSEEVENTF_XUP** flags simultaneously in the **dwFlags** parameter, because they both require use of the **mouseData** field. 

| Value | Meaning |
|-|-|
| **MOUSEEVENTF_MOVE**<br>0x0001 | Movement occurred. |
| **MOUSEEVENTF_LEFTDOWN**<br>0x0002 | The left button was pressed. |
| **MOUSEEVENTF_LEFTUP**<br>0x0004 | The left button was released. |
| **MOUSEEVENTF_RIGHTDOWN**<br>0x0008 | The right button was pressed. |
| **MOUSEEVENTF_RIGHTUP**<br>0x0010 | The right button was released. |
| **MOUSEEVENTF_MIDDLEDOWN**<br>0x0020 | The middle button was pressed. |
| **MOUSEEVENTF_MIDDLEUP**<br>0x0040 | The middle button was released. |
| **MOUSEEVENTF_XDOWN**<br>0x0080 | An X button was pressed. |
| **MOUSEEVENTF_XUP**<br>0x0100 | An X button was released. |
| **MOUSEEVENTF_WHEEL**<br>0x0800 | The wheel was moved, if the mouse has a wheel. The amount of movement is specified in **mouseData**. |
| **MOUSEEVENTF_HWHEEL**<br>0x1000 | The wheel was moved horizontally, if the mouse has a wheel. The amount of movement is specified in **mouseData**. <br>**Windows XP/2000**: This value is not supported. |
| **MOUSEEVENTF_MOVE_NOCOALESCE**<br>0x2000 | The [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove) messages will not be coalesced. The default behavior is to coalesce **WM_MOUSEMOVE** messages. <br>**Windows XP/2000**: This value is not supported. |
| **MOUSEEVENTF_VIRTUALDESK**<br>0x4000 | Maps coordinates to the entire desktop. Must be used with **MOUSEEVENTF_ABSOLUTE**. |
| **MOUSEEVENTF_ABSOLUTE**<br>0x8000 | The **dx** and **dy** members contain normalized absolute coordinates. If the flag is not set, **dx** and **dy** contain relative data (the change in position since the last reported position). This flag can be set, or not set, regardless of what kind of mouse or other pointing device, if any, is connected to the system. For further information about relative mouse motion, see the following Remarks section. |

### -field time

Type: **DWORD**

The time stamp for the event, in milliseconds. If this parameter is 0, the system will provide its own time stamp.

### -field dwExtraInfo

Type: **ULONG_PTR**

An additional value associated with the mouse event. An application calls [GetMessageExtraInfo](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo) to obtain this extra information.

## -remarks

If the mouse has moved, indicated by **MOUSEEVENTF_MOVE**, **dx** and **dy** specify information about that movement. The information is specified as absolute or relative integer values. 

If **MOUSEEVENTF_ABSOLUTE** value is specified, **dx** and **dy** contain normalized absolute coordinates between 0 and 65,535. The event procedure maps these coordinates onto the display surface. Coordinate (0,0) maps onto the upper-left corner of the display surface; coordinate (65535,65535) maps onto the lower-right corner. In a multimonitor system, the coordinates map to the primary monitor. 

If **MOUSEEVENTF_VIRTUALDESK** is specified, the coordinates map to the entire virtual desktop.

If the **MOUSEEVENTF_ABSOLUTE** value is not specified, **dx** and **dy** specify movement relative to the previous mouse event (the last reported position). Positive values mean the mouse moved right (or down); negative values mean the mouse moved left (or up). 

Relative mouse motion is subject to the effects of the mouse speed and the two-mouse threshold values. A user sets these three values with the **Pointer Speed** slider of the Control Panel's **Mouse Properties** sheet. You can obtain and set these values using the [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function. 

The system applies two tests to the specified relative mouse movement. If the specified distance along either the x or y axis is greater than the first mouse threshold value, and the mouse speed is not zero, the system doubles the distance. If the specified distance along either the x or y axis is greater than the second mouse threshold value, and the mouse speed is equal to two, the system doubles the distance that resulted from applying the first threshold test. It is thus possible for the system to multiply specified relative mouse movement along the x or y axis by up to four times.

## -see-also

**Conceptual**

[GetMessageExtraInfo](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo)

[INPUT](/windows/desktop/api/winuser/ns-winuser-input)

[Keyboard Input](/windows/desktop/inputdev/keyboard-input)

**Reference**

[SendInput](/windows/desktop/api/winuser/nf-winuser-sendinput)