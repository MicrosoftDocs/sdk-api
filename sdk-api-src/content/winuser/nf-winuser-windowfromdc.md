---
UID: NF:winuser.WindowFromDC
title: WindowFromDC function (winuser.h)
description: The WindowFromDC function returns a handle to the window associated with the specified display device context (DC). Output functions that use the specified device context draw into this window.
helpviewer_keywords: ["WindowFromDC","WindowFromDC function [Windows GDI]","_win32_WindowFromDC","gdi.windowfromdc","winuser/WindowFromDC"]
old-location: gdi\windowfromdc.htm
tech.root: gdi
ms.assetid: 57ecec82-03be-4d1a-84cf-6b64131af19d
ms.date: 12/05/2018
ms.keywords: WindowFromDC, WindowFromDC function [Windows GDI], _win32_WindowFromDC, gdi.windowfromdc, winuser/WindowFromDC
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
 - WindowFromDC
 - winuser/WindowFromDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-draw-l1-1-0.dll
 - user32.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - WindowFromDC
req.apiset: ext-ms-win-ntuser-draw-l1-1-1 (introduced in Windows 8.1)
---

# WindowFromDC function


## -description

The <b>WindowFromDC</b> function returns a handle to the window associated with the specified display device context (DC). Output functions that use the specified device context draw into this window.

## -parameters

### -param hDC [in]

Handle to the device context from which a handle to the associated window is to be retrieved.

## -returns

The return value is a handle to the window associated with the specified DC. If no window is associated with the specified DC, the return value is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdcex">GetDCEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowdc">GetWindowDC</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>
