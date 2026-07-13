---
UID: NF:winuser.RealChildWindowFromPoint
title: RealChildWindowFromPoint function (winuser.h)
description: Retrieves a handle to the child window at the specified point. The search is restricted to immediate child windows; grandchildren and deeper descendant windows are not searched.
helpviewer_keywords: ["RealChildWindowFromPoint","RealChildWindowFromPoint function [Windows and Messages]","_win32_RealChildWindowFromPoint","_win32_realchildwindowfrompoint_cpp","winmsg.realchildwindowfrompoint","winui._win32_realchildwindowfrompoint","winuser/RealChildWindowFromPoint"]
old-location: winmsg\realchildwindowfrompoint.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\realchildwindowfrompoint.htm
ms.date: 12/05/2018
ms.keywords: RealChildWindowFromPoint, RealChildWindowFromPoint function [Windows and Messages], _win32_RealChildWindowFromPoint, _win32_realchildwindowfrompoint_cpp, winmsg.realchildwindowfrompoint, winui._win32_realchildwindowfrompoint, winuser/RealChildWindowFromPoint
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
 - RealChildWindowFromPoint
 - winuser/RealChildWindowFromPoint
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
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
api_name:
 - RealChildWindowFromPoint
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# RealChildWindowFromPoint function


## -description

Retrieves a handle to the child window at the specified point. The search is restricted to immediate child windows; grandchildren and deeper descendant windows are not searched.

## -parameters

### -param hwndParent [in]

Type: <b>HWND</b>

A handle to the window whose child is to be retrieved.

### -param ptParentClientCoords [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that defines the client coordinates of the point to be checked.

## -returns

Type: <b>HWND</b>

The return value is a handle to the child window that contains the specified point.

## -remarks

<b>RealChildWindowFromPoint</b> treats <b>HTTRANSPARENT</b> areas of a standard control differently from other areas of the control; it returns the child window behind a transparent part of a control. In contrast, <a href="/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint">ChildWindowFromPoint</a> treats <b>HTTRANSPARENT</b> areas of a control the same as other areas. For example, if the point is in a transparent area of a groupbox, <b>RealChildWindowFromPoint</b> returns the child window behind a groupbox, whereas <b>ChildWindowFromPoint</b> returns the groupbox. However, both APIs return a static field, even though it, too, returns <b>HTTRANSPARENT</b>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint">ChildWindowFromPoint</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
