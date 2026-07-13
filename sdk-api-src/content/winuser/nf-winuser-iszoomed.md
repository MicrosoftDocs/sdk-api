---
UID: NF:winuser.IsZoomed
title: IsZoomed function (winuser.h)
description: Determines whether a window is maximized.
helpviewer_keywords: ["IsZoomed","IsZoomed function [Windows and Messages]","_win32_IsZoomed","_win32_iszoomed_cpp","winmsg.iszoomed","winui._win32_iszoomed","winuser/IsZoomed"]
old-location: winmsg\iszoomed.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\iszoomed.htm
ms.date: 12/05/2018
ms.keywords: IsZoomed, IsZoomed function [Windows and Messages], _win32_IsZoomed, _win32_iszoomed_cpp, winmsg.iszoomed, winui._win32_iszoomed, winuser/IsZoomed
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
 - IsZoomed
 - winuser/IsZoomed
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
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsZoomed
req.apiset: ext-ms-win-ntuser-window-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# IsZoomed function


## -description

Determines whether a window is maximized.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested.

## -returns

Type: <b>BOOL</b>

If the window is zoomed, the return value is nonzero.

If the window is not zoomed, the return value is zero.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-isiconic">IsIconic</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
