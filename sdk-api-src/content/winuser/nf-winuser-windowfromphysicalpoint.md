---
UID: NF:winuser.WindowFromPhysicalPoint
title: WindowFromPhysicalPoint function (winuser.h)
description: Retrieves a handle to the window that contains the specified physical point.
helpviewer_keywords: ["WindowFromPhysicalPoint","WindowFromPhysicalPoint function [Windows and Messages]","_win32_WindowFromPhysicalPoint","_win32_windowfromphysicalpoint_cpp","winmsg.windowfromphysicalpoint","winui._win32_windowfromphysicalpoint","winuser/WindowFromPhysicalPoint"]
old-location: winmsg\windowfromphysicalpoint.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\windowfromphysicalpoint.htm
ms.date: 12/05/2018
ms.keywords: WindowFromPhysicalPoint, WindowFromPhysicalPoint function [Windows and Messages], _win32_WindowFromPhysicalPoint, _win32_windowfromphysicalpoint_cpp, winmsg.windowfromphysicalpoint, winui._win32_windowfromphysicalpoint, winuser/WindowFromPhysicalPoint
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
 - WindowFromPhysicalPoint
 - winuser/WindowFromPhysicalPoint
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
 - WindowFromPhysicalPoint
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# WindowFromPhysicalPoint function


## -description

Retrieves a handle to the window that contains the specified physical point.

## -parameters

### -param Point [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The physical coordinates of the point.

## -returns

Type: <b>HWND</b>

A handle to the window that contains the given physical point. If no window exists at the point, this value is <b>NULL</b>.

## -remarks

The <b>WindowFromPhysicalPoint</b> function does not retrieve a handle to a hidden or disabled window, even if the point is within the window.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint">ChildWindowFromPoint</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-windowfromdc">WindowFromDC</a>



<a href="/windows/desktop/api/winuser/nf-winuser-windowfrompoint">WindowFromPoint</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
