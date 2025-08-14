---
UID: NF:winuser.DragDetect
title: DragDetect function (winuser.h)
description: Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.
helpviewer_keywords: ["DragDetect","DragDetect function [Keyboard and Mouse Input]","_win32_DragDetect","_win32_dragdetect_cpp","inputdev.dragdetect","winui._win32_dragdetect","winuser/DragDetect"]
old-location: inputdev\dragdetect.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\dragdetect.htm
ms.date: 12/05/2018
ms.keywords: DragDetect, DragDetect function [Keyboard and Mouse Input], _win32_DragDetect, _win32_dragdetect_cpp, inputdev.dragdetect, winui._win32_dragdetect, winuser/DragDetect
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
 - DragDetect
 - winuser/DragDetect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-rawinput-l1-2-0.dll
 - ext-ms-win-ntuser-rawinput-l1-1-0.dll
 - User32.dll
api_name:
 - DragDetect
---

# DragDetect function


## -description

Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point. The width and height of the drag rectangle are specified by the <b>SM_CXDRAG</b> and <b>SM_CYDRAG</b> values returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window receiving mouse input.

### -param pt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

Initial position of the mouse, in screen coordinates. The function determines the coordinates of the drag rectangle by using this point.

## -returns

Type: <b>BOOL</b>

If the user moved the mouse outside of the drag rectangle while holding down the left button, the return value is nonzero.

If the user did not move the mouse outside of the drag rectangle while holding down the left button, the return value is zero.

## -remarks

The system metrics for the drag rectangle are configurable, allowing for larger or smaller drag rectangles.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>