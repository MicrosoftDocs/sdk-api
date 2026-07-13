---
UID: NF:winuser.GetWindowRgnBox
title: GetWindowRgnBox function (winuser.h)
description: The GetWindowRgnBox function retrieves the dimensions of the tightest bounding rectangle for the window region of a window.
helpviewer_keywords: ["GetWindowRgnBox","GetWindowRgnBox function [Windows GDI]","_win32_GetWindowRgnBox","gdi.getwindowrgnbox","winuser/GetWindowRgnBox"]
old-location: gdi\getwindowrgnbox.htm
tech.root: gdi
ms.assetid: 20e23474-a1c5-4afe-976e-a7e5790fb91b
ms.date: 12/05/2018
ms.keywords: GetWindowRgnBox, GetWindowRgnBox function [Windows GDI], _win32_GetWindowRgnBox, gdi.getwindowrgnbox, winuser/GetWindowRgnBox
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
 - GetWindowRgnBox
 - winuser/GetWindowRgnBox
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - GetWindowRgnBox
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# GetWindowRgnBox function


## -description

The <b>GetWindowRgnBox</b> function retrieves the dimensions of the tightest bounding rectangle for the window region of a window.

## -parameters

### -param hWnd [in]

Handle to the window.

### -param lprc [out]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the rectangle dimensions, in device units relative to the upper-left corner of the window.

## -returns

The return value specifies the type of the region that the function obtains. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>The region is more than one rectangle.</td>
</tr>
<tr>
<td>ERROR</td>
<td>The specified window does not have a region, or an error occurred while attempting to return the region.</td>
</tr>
<tr>
<td>NULLREGION</td>
<td>The region is empty.</td>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>The region is a single rectangle.</td>
</tr>
</table>

## -remarks

The window region determines the area within the window where the system permits drawing. The system does not display any portion of a window that lies outside of the window region. The coordinates of a window's window region are relative to the upper-left corner of the window, not the client area of the window.

To set the window region of a window, call the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowrgn">SetWindowRgn</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-getclipbox">GetClipBox</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowrgn">GetWindowRgn</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowrgn">SetWindowRgn</a>
