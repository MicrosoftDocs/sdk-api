---
UID: NF:winuser.LogicalToPhysicalPoint
title: LogicalToPhysicalPoint function (winuser.h)
description: Converts the logical coordinates of a point in a window to physical coordinates.
helpviewer_keywords: ["LogicalToPhysicalPoint","LogicalToPhysicalPoint function [Windows and Messages]","_win32_LogicalToPhysicalPoint","_win32_logicaltophysicalpoint_cpp","winmsg.logicaltophysicalpoint","winui._win32_logicaltophysicalpoint","winuser/LogicalToPhysicalPoint"]
old-location: winmsg\logicaltophysicalpoint.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\logicaltophysicalpoint.htm
ms.date: 12/05/2018
ms.keywords: LogicalToPhysicalPoint, LogicalToPhysicalPoint function [Windows and Messages], _win32_LogicalToPhysicalPoint, _win32_logicaltophysicalpoint_cpp, winmsg.logicaltophysicalpoint, winui._win32_logicaltophysicalpoint, winuser/LogicalToPhysicalPoint
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
 - LogicalToPhysicalPoint
 - winuser/LogicalToPhysicalPoint
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
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - LogicalToPhysicalPoint
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# LogicalToPhysicalPoint function


## -description

Converts the logical coordinates of a point in a window to physical coordinates.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose transform is used for the conversion. Top level windows are fully supported. In the case of child windows, only the area of overlap between the parent and the child window is converted.

### -param lpPoint [in, out]

Type: <b>LPPOINT</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that specifies the logical coordinates to be converted. The new physical coordinates are copied into this structure if the function succeeds.

## -remarks

Windows Vista introduces the concept of physical coordinates. Desktop Window Manager (DWM) scales non-dots per inch (dpi) aware windows when the display is high dpi. The window seen on the screen corresponds to the physical coordinates. The application continues to work in logical space. Therefore, the application's view of the window is different from that which appears on the screen. For scaled windows, logical and physical coordinates are different.

<b>LogicalToPhysicalPoint</b> is a transformation API that can be called by a process that declares itself as dpi aware. The function uses the window identified by the <i>hWnd</i> parameter and the logical coordinates given in the <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure to compute the physical coordinates.

The <b>LogicalToPhysicalPoint</b> function replaces the logical coordinates in the <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure with the physical coordinates. The physical coordinates are relative to the upper-left corner of the screen. The coordinates have to be inside the client area of <i>hWnd</i>.

On all platforms, <b>LogicalToPhysicalPoint</b> will fail on a window that has either 0 width or height; an application must first establish a non-0 width and height by calling, for example, <a href="/windows/desktop/api/winuser/nf-winuser-movewindow">MoveWindow</a>.  On some versions of Windows (including Windows 7), <b>LogicalToPhysicalPoint</b> will still fail if <b>MoveWindow</b> has been called after a call to <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> with <b>SH_HIDE</b> has hidden the window.

In Windows 8, system–DPI aware applications translate between physical and logical space using PhysicalToLogicalPoint and LogicalToPhysicalPoint. In Windows 8.1, the additional virtualization of the system and inter-process communications means that for the majority of applications, you do not need these APIs. As a result, in Windows 8.1, PhysicalToLogicalPoint and LogicalToPhysicalPoint no longer transform points. The system returns all points to an application in its own coordinate space. 
This behavior preserves functionality for the majority of applications, but there are some exceptions in which you must make changes to ensure that the application works as expected.
In those cases, use <a href="/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi">PhysicalToLogicalPointForPerMonitorDPI</a> and <a href="/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi">LogicalToPhysicalPointForPerMonitorDPI.</a>
