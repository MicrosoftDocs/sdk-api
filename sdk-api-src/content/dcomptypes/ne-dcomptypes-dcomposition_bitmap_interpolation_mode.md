---
UID: NE:dcomptypes.DCOMPOSITION_BITMAP_INTERPOLATION_MODE
title: DCOMPOSITION_BITMAP_INTERPOLATION_MODE (dcomptypes.h)
description: Specifies the interpolation mode to be used when a bitmap is composed with any transform where the pixels in the bitmap don't line up exactly one-to-one with pixels on screen.
helpviewer_keywords: ["DCOMPOSITION_BITMAP_INTERPOLATION_MODE","DCOMPOSITION_BITMAP_INTERPOLATION_MODE enumeration [DirectComposition]","DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT","DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR","DCOMPOSITION_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR","dcomptypes/DCOMPOSITION_BITMAP_INTERPOLATION_MODE","dcomptypes/DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT","dcomptypes/DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR","dcomptypes/DCOMPOSITION_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR","directcomp.dcomposition_bitmap_interpolation_mode"]
old-location: directcomp\dcomposition_bitmap_interpolation_mode.htm
tech.root: directcomp
ms.assetid: 0B919A5C-DEDD-4131-B743-A61CA49CA2B6
ms.date: 12/05/2018
ms.keywords: DCOMPOSITION_BITMAP_INTERPOLATION_MODE, DCOMPOSITION_BITMAP_INTERPOLATION_MODE enumeration [DirectComposition], DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT, DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR, DCOMPOSITION_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR, dcomptypes/DCOMPOSITION_BITMAP_INTERPOLATION_MODE, dcomptypes/DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT, dcomptypes/DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR, dcomptypes/DCOMPOSITION_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR, directcomp.dcomposition_bitmap_interpolation_mode
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
 - DCOMPOSITION_BITMAP_INTERPOLATION_MODE
 - dcomptypes/DCOMPOSITION_BITMAP_INTERPOLATION_MODE
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
 - DCOMPOSITION_BITMAP_INTERPOLATION_MODE
---

# DCOMPOSITION_BITMAP_INTERPOLATION_MODE enumeration


## -description

Specifies the interpolation mode to be used when a bitmap is composed with any transform where the pixels in the bitmap don't line up exactly one-to-one with pixels on screen.

## -enum-fields

### -field DCOMPOSITION_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR:0

Bitmaps are interpolated by using nearest-neighbor sampling.

### -field DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR:1

Bitmaps are interpolated by using linear sampling.

### -field DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT:0xffffffff

Bitmaps are interpolated according to the mode established by the parent visual.

## -remarks

The default interpolation mode for a visual is <b>DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT</b>. If all visuals in a visual tree specify this mode, the default for all visuals is nearest neighbor sampling, which is the fastest mode.

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
If you want a visual to be drawn with antialiasing, use <b>DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR</b> for the content of the visual, and <a href="/windows/desktop/api/dcomptypes/ne-dcomptypes-dcomposition_border_mode">DCOMPOSITION_BORDER_MODE_SOFT</a> for the edges.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode">IDCompositionVisual::SetBitmapInterpolationMode</a>
