---
UID: NF:wingdi.Rectangle
title: Rectangle function (wingdi.h)
description: The Rectangle function draws a rectangle. The rectangle is outlined by using the current pen and filled by using the current brush.
helpviewer_keywords: ["Rectangle","Rectangle function [Windows GDI]","_win32_Rectangle","gdi.rectangle","wingdi/Rectangle"]
old-location: gdi\rectangle.htm
tech.root: gdi
ms.assetid: ed6b9824-1edc-4510-b9da-a4287845aa83
ms.date: 12/05/2018
ms.keywords: Rectangle, Rectangle function [Windows GDI], _win32_Rectangle, gdi.rectangle, wingdi/Rectangle
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
 - Rectangle
 - wingdi/Rectangle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - Rectangle
---

# Rectangle function


## -description

The <b>Rectangle</b> function draws a rectangle. The rectangle is outlined by using the current pen and filled by using the current brush.

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

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The current position is neither used nor updated by <b>Rectangle</b>.

The rectangle that is drawn excludes the bottom and right edges.

If a PS_NULL pen is used, the dimensions of the rectangle are 1 pixel less in height and 1 pixel less in width.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-filled-shapes">Using Filled Shapes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/filled-shape-functions">Filled Shape Functions</a>



<a href="/windows/desktop/gdi/filled-shapes">Filled Shapes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-roundrect">RoundRect
      </a>