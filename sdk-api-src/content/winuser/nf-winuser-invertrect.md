---
UID: NF:winuser.InvertRect
title: InvertRect function (winuser.h)
description: The InvertRect function inverts a rectangle in a window by performing a logical NOT operation on the color values for each pixel in the rectangle's interior.
helpviewer_keywords: ["InvertRect","InvertRect function [Windows GDI]","_win32_InvertRect","gdi.invertrect","winuser/InvertRect"]
old-location: gdi\invertrect.htm
tech.root: gdi
ms.assetid: a8c4dbf1-94ec-46e9-b365-7dfc89e4f176
ms.date: 12/05/2018
ms.keywords: InvertRect, InvertRect function [Windows GDI], _win32_InvertRect, gdi.invertrect, winuser/InvertRect
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
 - InvertRect
 - winuser/InvertRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-gui-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-gui-l1-1-0.dll
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - user32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - InvertRect
req.apiset: ext-ms-win-ntuser-gui-l1-1-1 (introduced in Windows 8.1)
---

# InvertRect function


## -description

The <b>InvertRect</b> function inverts a rectangle in a window by performing a logical NOT operation on the color values for each pixel in the rectangle's interior.

## -parameters

### -param hDC [in]

A handle to the device context.

### -param lprc [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the rectangle to be inverted.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

On monochrome screens, <b>InvertRect</b> makes white pixels black and black pixels white. On color screens, the inversion depends on how colors are generated for the screen. Calling <b>InvertRect</b> twice for the same rectangle restores the display to its previous colors.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-fillrect">FillRect
      </a>



<a href="/windows/desktop/gdi/filled-shape-functions">Filled Shape Functions</a>



<a href="/windows/desktop/gdi/filled-shapes">Filled Shapes Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT
      </a>
