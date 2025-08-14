---
UID: NF:winuser.GetUpdateRect
title: GetUpdateRect function (winuser.h)
description: The GetUpdateRect function retrieves the coordinates of the smallest rectangle that completely encloses the update region of the specified window.
helpviewer_keywords: ["GetUpdateRect","GetUpdateRect function [Windows GDI]","_win32_GetUpdateRect","gdi.getupdaterect","winuser/GetUpdateRect"]
old-location: gdi\getupdaterect.htm
tech.root: gdi
ms.assetid: e54483a1-8738-4b22-a24e-c0b31f6ca9d6
ms.date: 12/05/2018
ms.keywords: GetUpdateRect, GetUpdateRect function [Windows GDI], _win32_GetUpdateRect, gdi.getupdaterect, winuser/GetUpdateRect
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
 - GetUpdateRect
 - winuser/GetUpdateRect
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
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - GetUpdateRect
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# GetUpdateRect function


## -description

The <b>GetUpdateRect</b> function retrieves the coordinates of the smallest rectangle that completely encloses the update region of the specified window. <b>GetUpdateRect</b> retrieves the rectangle in logical coordinates. If there is no update region, <b>GetUpdateRect</b> retrieves an empty rectangle (sets all coordinates to zero).

## -parameters

### -param hWnd [in]

Handle to the window whose update region is to be retrieved.

### -param lpRect [out]

Pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the coordinates, in device units, of the enclosing rectangle.

An application can set this parameter to <b>NULL</b> to determine whether an update region exists for the window. If this parameter is <b>NULL</b>, <b>GetUpdateRect</b> returns nonzero if an update region exists, and zero if one does not. This provides a simple and efficient means of determining whether a <b>WM_PAINT</b> message resulted from an invalid area.

### -param bErase [in]

Specifies whether the background in the update region is to be erased. If this parameter is <b>TRUE</b> and the update region is not empty, <b>GetUpdateRect</b> sends a <b>WM_ERASEBKGND</b> message to the specified window to erase the background.

## -returns

If the update region is not empty, the return value is nonzero.

If there is no update region, the return value is zero.

## -remarks

The update rectangle retrieved by the <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function is identical to that retrieved by <b>GetUpdateRect</b>.


<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> automatically validates the update region, so any call to <b>GetUpdateRect</b> made immediately after the call to <b>BeginPaint</b> retrieves an empty update region.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getupdatergn">GetUpdateRgn</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-validaterect">ValidateRect</a>
