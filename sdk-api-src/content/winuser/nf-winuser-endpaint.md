---
UID: NF:winuser.EndPaint
title: EndPaint function (winuser.h)
description: The EndPaint function marks the end of painting in the specified window. This function is required for each call to the BeginPaint function, but only after painting is complete.
helpviewer_keywords: ["EndPaint","EndPaint function [Windows GDI]","_win32_EndPaint","gdi.endpaint","winuser/EndPaint"]
old-location: gdi\endpaint.htm
tech.root: gdi
ms.assetid: b07cfed9-21c4-4459-855a-eaf4d1d34ab8
ms.date: 12/05/2018
ms.keywords: EndPaint, EndPaint function [Windows GDI], _win32_EndPaint, gdi.endpaint, winuser/EndPaint
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
 - EndPaint
 - winuser/EndPaint
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
 - EndPaint
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# EndPaint function


## -description

The <b>EndPaint</b> function marks the end of painting in the specified window. This function is required for each call to the <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function, but only after painting is complete.

## -parameters

### -param hWnd [in]

Handle to the window that has been repainted.

### -param lpPaint [in]

Pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-paintstruct">PAINTSTRUCT</a> structure that contains the painting information retrieved by <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>.

## -returns

The return value is always nonzero.

## -remarks

If the caret was hidden by <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>, <b>EndPaint</b> restores the caret to the screen.

<b>EndPaint</b> releases the display device context that <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> retrieved.


#### Examples

For an example, see <a href="/windows/desktop/gdi/drawing-in-the-client-area">Drawing in the Client Area</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/api/winuser/ns-winuser-paintstruct">PAINTSTRUCT</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>
