---
UID: NS:wingdi._GRADIENT_TRIANGLE
title: GRADIENT_TRIANGLE (wingdi.h)
description: The GRADIENT_TRIANGLE structure specifies the index of three vertices in the pVertex array in the GradientFill function. These three vertices form one triangle.
helpviewer_keywords: ["*LPGRADIENT_TRIANGLE","*PGRADIENT_TRIANGLE","GRADIENT_TRIANGLE","GRADIENT_TRIANGLE structure [Windows GDI]","PGRADIENT_TRIANGLE","PGRADIENT_TRIANGLE structure pointer [Windows GDI]","_win32_GRADIENT_TRIANGLE_str","gdi.gradient_triangle","wingdi/GRADIENT_TRIANGLE","wingdi/PGRADIENT_TRIANGLE"]
old-location: gdi\gradient_triangle.htm
tech.root: gdi
ms.assetid: 71f3a4bd-5823-47ae-aa7a-f3058f18c591
ms.date: 12/05/2018
ms.keywords: '*LPGRADIENT_TRIANGLE, *PGRADIENT_TRIANGLE, GRADIENT_TRIANGLE, GRADIENT_TRIANGLE structure [Windows GDI], PGRADIENT_TRIANGLE, PGRADIENT_TRIANGLE structure pointer [Windows GDI], _win32_GRADIENT_TRIANGLE_str, gdi.gradient_triangle, wingdi/GRADIENT_TRIANGLE, wingdi/PGRADIENT_TRIANGLE'
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
req.typenames: GRADIENT_TRIANGLE, *PGRADIENT_TRIANGLE, *LPGRADIENT_TRIANGLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GRADIENT_TRIANGLE
 - wingdi/_GRADIENT_TRIANGLE
 - PGRADIENT_TRIANGLE
 - wingdi/PGRADIENT_TRIANGLE
 - GRADIENT_TRIANGLE
 - wingdi/GRADIENT_TRIANGLE
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
 - GRADIENT_TRIANGLE
---

# GRADIENT_TRIANGLE structure


## -description

The <b>GRADIENT_TRIANGLE</b> structure specifies the index of three vertices in the <i>pVertex</i> array in the <b>GradientFill</b> function. These three vertices form one triangle.

## -struct-fields

### -field Vertex1

The first point of the triangle where sides intersect.

### -field Vertex2

The second point of the triangle where sides intersect.

### -field Vertex3

The third point of the triangle where sides intersect.

## -remarks

The <b>GRADIENT_TRIANGLE</b> structure specifies the values in the <i>pVertex</i> array that are used when the <i>dwMode</i> parameter of the <a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a> function is GRADIENT_FILL_TRIANGLE. For related <b>GradientFill</b> structures, see <a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_rect">GRADIENT_RECT</a> and <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a>.

The following image shows an example of a triangle with a gradient fill.

<img alt="Illustration of a triangle that fills from orange at the top point to magenta on the bottom line " border="0" src="images/GradientFillTriangle.png"/>

#### Examples

For an example, see <a href="/windows/desktop/gdi/drawing-a-shaded-triangle">Drawing a Shaded Triangle</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_rect">GRADIENT_RECT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a>