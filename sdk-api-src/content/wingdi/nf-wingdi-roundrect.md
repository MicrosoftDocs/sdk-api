---
UID: NF:wingdi.RoundRect
title: RoundRect function (wingdi.h)
description: The RoundRect function draws a rectangle with rounded corners. The rectangle is outlined by using the current pen and filled by using the current brush.
helpviewer_keywords: ["RoundRect","RoundRect function [Windows GDI]","_win32_RoundRect","gdi.roundrect","wingdi/RoundRect"]
old-location: gdi\roundrect.htm
tech.root: gdi
ms.assetid: 17808a6a-7bd0-4fd6-81ab-00d5db764b93
ms.date: 12/05/2018
ms.keywords: RoundRect, RoundRect function [Windows GDI], _win32_RoundRect, gdi.roundrect, wingdi/RoundRect
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoundRect
 - wingdi/RoundRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - RoundRect
---

# RoundRect function


## -description

The <b>RoundRect</b> function draws a rectangle with rounded corners. The rectangle is outlined by using the current pen and filled by using the current brush.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param left [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the rectangle.

### -param top [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the rectangle.

### -param right [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the rectangle.

### -param bottom [in]

The y-coordinate, in logical coordinates, of the lower-right corner of the rectangle.

### -param width [in]

The width, in logical coordinates, of the ellipse used to draw the rounded corners.

### -param height [in]

The height, in logical coordinates, of the ellipse used to draw the rounded corners.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The current position is neither used nor updated by this function.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-filled-shapes">Using Filled Shapes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/filled-shape-functions">Filled Shape Functions</a>



<a href="/windows/desktop/gdi/filled-shapes">Filled Shapes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rectangle">Rectangle
      </a>