---
UID: NE:dcomptypes.DCOMPOSITION_BORDER_MODE
title: DCOMPOSITION_BORDER_MODE (dcomptypes.h)
description: Specifies the border mode to use when composing a bitmap or applying a clip with any transform such that the edges of the bitmap or clip are not axis-aligned with integer coordinates.
helpviewer_keywords: ["DCOMPOSITION_BORDER_MODE","DCOMPOSITION_BORDER_MODE enumeration [DirectComposition]","DCOMPOSITION_BORDER_MODE_HARD","DCOMPOSITION_BORDER_MODE_INHERIT","DCOMPOSITION_BORDER_MODE_SOFT","dcomptypes/DCOMPOSITION_BORDER_MODE","dcomptypes/DCOMPOSITION_BORDER_MODE_HARD","dcomptypes/DCOMPOSITION_BORDER_MODE_INHERIT","dcomptypes/DCOMPOSITION_BORDER_MODE_SOFT","directcomp.dcomposition_border_mode"]
old-location: directcomp\dcomposition_border_mode.htm
tech.root: directcomp
ms.assetid: 26CDDC8A-27F5-4BE4-B345-70FF66ED5C9A
ms.date: 12/05/2018
ms.keywords: DCOMPOSITION_BORDER_MODE, DCOMPOSITION_BORDER_MODE enumeration [DirectComposition], DCOMPOSITION_BORDER_MODE_HARD, DCOMPOSITION_BORDER_MODE_INHERIT, DCOMPOSITION_BORDER_MODE_SOFT, dcomptypes/DCOMPOSITION_BORDER_MODE, dcomptypes/DCOMPOSITION_BORDER_MODE_HARD, dcomptypes/DCOMPOSITION_BORDER_MODE_INHERIT, dcomptypes/DCOMPOSITION_BORDER_MODE_SOFT, directcomp.dcomposition_border_mode
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
 - DCOMPOSITION_BORDER_MODE
 - dcomptypes/DCOMPOSITION_BORDER_MODE
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
 - DCOMPOSITION_BORDER_MODE
---

# DCOMPOSITION_BORDER_MODE enumeration


## -description

Specifies the border mode to use when composing a bitmap or applying a clip with any transform such that the edges of the bitmap or clip are not axis-aligned with integer coordinates.

## -enum-fields

### -field DCOMPOSITION_BORDER_MODE_SOFT:0

Bitmap and clip edges are antialiased.

### -field DCOMPOSITION_BORDER_MODE_HARD:1

Bitmap and clip edges are aliased. See Remarks.

### -field DCOMPOSITION_BORDER_MODE_INHERIT:0xffffffff

Bitmap and clip edges are drawn according to the mode established by the parent visual.

## -remarks

The default border mode for any given visual is <b>DCOMPOSITION_BORDER_MODE_INHERIT</b>, which delegates the determination of the border mode to the parent visual. If all visuals in a visual tree specify this mode, the default for all visuals is aliased rendering, which is the fastest mode.

A single visual can have any combination of visual properties. However, if a 
visual has the following combination of properties, the borders of the visual will default 
to <b>DCOMPOSITION_BORDER_MODE_HARD</b>.



<ul>
<li><code>SetCompositeMode(DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT)
</code></li>
<li><code>SetBorderMode(DCOMPOSITION_BORDER_MODE_SOFT) 
</code></li>
<li><code>SetBitmapInterpolationMode(DCOMPOSITION_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR)</code></li>
</ul>
If you want a visual to be drawn with antialiasing, use <a href="/windows/desktop/api/dcomptypes/ne-dcomptypes-dcomposition_bitmap_interpolation_mode">DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR</a> for the content of the visual, and <b>DCOMPOSITION_BORDER_MODE_SOFT</b> for the edges.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode">IDCompositionVisual::SetBorderMode</a>
