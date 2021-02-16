---
UID: NS:wingdi._GRADIENT_RECT
title: GRADIENT_RECT (wingdi.h)
description: The GRADIENT_RECT structure specifies the index of two vertices in the pVertex array in the GradientFill function. These two vertices form the upper-left and lower-right boundaries of a rectangle.
helpviewer_keywords: ["*LPGRADIENT_RECT","*PGRADIENT_RECT","GRADIENT_RECT","GRADIENT_RECT structure [Windows GDI]","PGRADIENT_RECT","PGRADIENT_RECT structure pointer [Windows GDI]","_win32_GRADIENT_RECT_str","gdi.gradient_rect","wingdi/GRADIENT_RECT","wingdi/PGRADIENT_RECT"]
old-location: gdi\gradient_rect.htm
tech.root: gdi
ms.assetid: 8660114a-423f-40a8-b113-e0304bb0f383
ms.date: 12/05/2018
ms.keywords: '*LPGRADIENT_RECT, *PGRADIENT_RECT, GRADIENT_RECT, GRADIENT_RECT structure [Windows GDI], PGRADIENT_RECT, PGRADIENT_RECT structure pointer [Windows GDI], _win32_GRADIENT_RECT_str, gdi.gradient_rect, wingdi/GRADIENT_RECT, wingdi/PGRADIENT_RECT'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GRADIENT_RECT, *PGRADIENT_RECT, *LPGRADIENT_RECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GRADIENT_RECT
 - wingdi/_GRADIENT_RECT
 - PGRADIENT_RECT
 - wingdi/PGRADIENT_RECT
 - GRADIENT_RECT
 - wingdi/GRADIENT_RECT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - GRADIENT_RECT
---

# GRADIENT_RECT structure


## -description

The <b>GRADIENT_RECT</b> structure specifies the index of two vertices in the <i>pVertex</i> array in the <b>GradientFill</b> function. These two vertices form the upper-left and lower-right boundaries of a rectangle.

## -struct-fields

### -field UpperLeft

The upper-left corner of a rectangle.

### -field LowerRight

The lower-right corner of a rectangle.

## -remarks

The <b>GRADIENT_RECT</b> structure specifies the values of the <i>pVertex</i> array that are used when the <i>dwMode</i> parameter of the <a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a> function is GRADIENT_FILL_RECT_H or GRADIENT_FILL_RECT_V. For related <b>GradientFill</b> structures, see <a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_triangle">GRADIENT_TRIANGLE</a> and <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a>.

The following images shows examples of a rectangle with a gradient fill - one in horizontal mode, the other in vertical mode.

<img alt="Illustration of a rectangle that shades from dark on the left side to light on the right side" border="0" src="images/GradientFillRectangle.png"/>
<img alt="Illustration of a rectangle that shades from dark on the top to light on the bottom" border="0" src="images/GradientFillRectangle2.png"/>

#### Examples

For an example, see <a href="/windows/desktop/gdi/drawing-a-shaded-rectangle">Drawing a Shaded Rectangle</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_triangle">GRADIENT_TRIANGLE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a>