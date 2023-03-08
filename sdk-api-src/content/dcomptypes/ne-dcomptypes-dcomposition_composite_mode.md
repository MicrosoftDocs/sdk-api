---
UID: NE:dcomptypes.DCOMPOSITION_COMPOSITE_MODE
title: DCOMPOSITION_COMPOSITE_MODE (dcomptypes.h)
description: The mode to use to blend the bitmap content of a visual with the render target.
helpviewer_keywords: ["DCOMPOSITION_COMPOSITE_MODE","DCOMPOSITION_COMPOSITE_MODE enumeration [DirectComposition]","DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT","DCOMPOSITION_COMPOSITE_MODE_INHERIT","DCOMPOSITION_COMPOSITE_MODE_MIN_BLEND","DCOMPOSITION_COMPOSITE_MODE_SOURCE_OVER","dcomptypes/DCOMPOSITION_COMPOSITE_MODE","dcomptypes/DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT","dcomptypes/DCOMPOSITION_COMPOSITE_MODE_INHERIT","dcomptypes/DCOMPOSITION_COMPOSITE_MODE_MIN_BLEND","dcomptypes/DCOMPOSITION_COMPOSITE_MODE_SOURCE_OVER","directcomp.dcomposition_composite_mode"]
old-location: directcomp\dcomposition_composite_mode.htm
tech.root: directcomp
ms.assetid: D89379F5-57F8-4838-8E8F-FF261D69DE59
ms.date: 12/05/2018
ms.keywords: DCOMPOSITION_COMPOSITE_MODE, DCOMPOSITION_COMPOSITE_MODE enumeration [DirectComposition], DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT, DCOMPOSITION_COMPOSITE_MODE_INHERIT, DCOMPOSITION_COMPOSITE_MODE_MIN_BLEND, DCOMPOSITION_COMPOSITE_MODE_SOURCE_OVER, dcomptypes/DCOMPOSITION_COMPOSITE_MODE, dcomptypes/DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT, dcomptypes/DCOMPOSITION_COMPOSITE_MODE_INHERIT, dcomptypes/DCOMPOSITION_COMPOSITE_MODE_MIN_BLEND, dcomptypes/DCOMPOSITION_COMPOSITE_MODE_SOURCE_OVER, directcomp.dcomposition_composite_mode
req.header: dcomptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DCOMPOSITION_COMPOSITE_MODE
 - dcomptypes/DCOMPOSITION_COMPOSITE_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DcompTypes.h
api_name:
 - DCOMPOSITION_COMPOSITE_MODE
---

# DCOMPOSITION_COMPOSITE_MODE enumeration


## -description

The mode to use to blend the bitmap content of a visual with  the render target.

## -enum-fields

### -field DCOMPOSITION_COMPOSITE_MODE_SOURCE_OVER:0

The standard source-over-destination blend mode.

### -field DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT:1

The bitmap colors are inverted.

### -field DCOMPOSITION_COMPOSITE_MODE_MIN_BLEND:2

Bitmap colors subtract for color channels in the background.

### -field DCOMPOSITION_COMPOSITE_MODE_INHERIT:0xffffffff

Bitmaps are blended according to the mode established by the parent visual.

## -remarks

A single visual can have any combination of visual properties. However, if a 
visual has the following combination of properties, the borders of the visual will default 
to <a href="/windows/desktop/api/dcomptypes/ne-dcomptypes-dcomposition_border_mode">DCOMPOSITION_BORDER_MODE_HARD</a>.



<ul>
<li><code>SetCompositeMode(DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT)
</code></li>
<li><code>SetBorderMode(DCOMPOSITION_BORDER_MODE_SOFT) 
</code></li>
<li><code>SetBitmapInterpolationMode(DCOMPOSITION_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR)</code></li>
</ul>
If you want a visual to be drawn with antialiasing, use <a href="/windows/desktop/api/dcomptypes/ne-dcomptypes-dcomposition_bitmap_interpolation_mode">DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR</a> for the content of the visual, and <a href="/windows/desktop/api/dcomptypes/ne-dcomptypes-dcomposition_border_mode">DCOMPOSITION_BORDER_MODE_SOFT</a> for the edges.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode">IDCompositionVisual::SetCompositeMode</a>
