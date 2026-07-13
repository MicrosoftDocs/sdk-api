---
UID: NF:winuser.PhysicalToLogicalPoint
title: PhysicalToLogicalPoint function (winuser.h)
description: Converts the physical coordinates of a point in a window to logical coordinates.
helpviewer_keywords: ["PhysicalToLogicalPoint","PhysicalToLogicalPoint function [Windows and Messages]","_win32_PhysicalToLogicalPoint","_win32_physicaltologicalpoint_cpp","winmsg.physicaltologicalpoint","winui._win32_physicaltologicalpoint","winuser/PhysicalToLogicalPoint"]
old-location: winmsg\physicaltologicalpoint.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\physicaltologicalpoint.htm
ms.date: 12/05/2018
ms.keywords: PhysicalToLogicalPoint, PhysicalToLogicalPoint function [Windows and Messages], _win32_PhysicalToLogicalPoint, _win32_physicaltologicalpoint_cpp, winmsg.physicaltologicalpoint, winui._win32_physicaltologicalpoint, winuser/PhysicalToLogicalPoint
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - PhysicalToLogicalPoint
 - winuser/PhysicalToLogicalPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - ext-ms-win-ntuser-window-l1-1-4.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - ext-ms-win-ntuser-window-l1-1-2.dll
 - User32.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
api_name:
 - PhysicalToLogicalPoint
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# PhysicalToLogicalPoint function


## -description

Converts the physical coordinates of a point in a window to logical coordinates.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose transform is used for the conversion. Top level windows are fully supported. In the case of child windows, only the area of overlap between the parent and the child window is converted.

### -param lpPoint [in, out]

Type: <b>LPPOINT</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that specifies the physical/screen coordinates to be converted. The new logical coordinates are copied into this structure if the function succeeds.

## -remarks

Windows Vista introduces the concept of physical coordinates. Desktop Window Manager (DWM) scales non-dots per inch (dpi) aware windows when the display is high dpi. The window seen on the screen corresponds to the physical coordinates. The application continues to work in logical space. Therefore, the application's view of the window is different from that which appears on the screen. For scaled windows, logical and physical coordinates are different.

The function uses the window identified by the <i>hWnd</i> parameter and the physical coordinates given in the <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure to compute the logical coordinates. The logical coordinates are the <i>unscaled</i> coordinates that appear to the application in a programmatic way. In other words, the logical coordinates are the coordinates the application recognizes, which can be different from the physical coordinates. The API then replaces the physical coordinates with the logical coordinates. The new coordinates are in the <i>world</i> coordinates whose origin is (0, 0) on the desktop. The coordinates passed to the API have to be on the <i>hWnd</i>.

The source coordinates are in device units.

On all platforms, <b>PhysicalToLogicalPoint</b> will fail on a window that has either 0 width or height; an application must first establish a non-0 width and height by calling, for example, <a href="/windows/desktop/api/winuser/nf-winuser-movewindow">MoveWindow</a>.  On some versions of Windows (including Windows 7), <b>PhysicalToLogicalPoint</b> will still fail if <b>MoveWindow</b> has been called after a call to <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> with <b>SH_HIDE</b> has hidden the window.

In Windows 8, system–DPI aware applications translate between physical and logical space using PhysicalToLogicalPoint and LogicalToPhysicalPoint. In Windows 8.1, the additional virtualization of the system and inter-process communications means that for the majority of applications, you do not need these APIs. As a result, in Windows 8.1, PhysicalToLogicalPoint and LogicalToPhysicalPoint no longer transform points. The system returns all points to an application in its own coordinate space. 
This behavior preserves functionality for the majority of applications, but there are some exceptions in which you must make changes to ensure that the application works as expected.
In those cases, use <a href="/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi">PhysicalToLogicalPointForPerMonitorDPI</a> and <a href="/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi">LogicalToPhysicalPointForPerMonitorDPI.</a>
