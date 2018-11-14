---
UID: NE:dcomptypes.DCOMPOSITION_COMPOSITE_MODE
title: DCOMPOSITION_COMPOSITE_MODE
author: windows-sdk-content
description: The mode to use to blend the bitmap content of a visual with the render target.
old-location: directcomp\dcomposition_composite_mode.htm
tech.root: directcomp
ms.assetid: D89379F5-57F8-4838-8E8F-FF261D69DE59
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DCOMPOSITION_COMPOSITE_MODE, DCOMPOSITION_COMPOSITE_MODE enumeration [DirectComposition], DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT, DCOMPOSITION_COMPOSITE_MODE_INHERIT, DCOMPOSITION_COMPOSITE_MODE_MIN_BLEND, DCOMPOSITION_COMPOSITE_MODE_SOURCE_OVER, dcomptypes/DCOMPOSITION_COMPOSITE_MODE, dcomptypes/DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT, dcomptypes/DCOMPOSITION_COMPOSITE_MODE_INHERIT, dcomptypes/DCOMPOSITION_COMPOSITE_MODE_MIN_BLEND, dcomptypes/DCOMPOSITION_COMPOSITE_MODE_SOURCE_OVER, directcomp.dcomposition_composite_mode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DcompTypes.h
api_name:
 - DCOMPOSITION_COMPOSITE_MODE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DCOMPOSITION_COMPOSITE_MODE enumeration


## -description


The mode to use to blend the bitmap content of a visual with  the render target.


## -enum-fields




### -field DCOMPOSITION_COMPOSITE_MODE_SOURCE_OVER

The standard source-over-destination blend mode.


### -field DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT

The bitmap colors are inverted.  


### -field DCOMPOSITION_COMPOSITE_MODE_MIN_BLEND

Bitmap colors subtract for color channels in the background.  


### -field DCOMPOSITION_COMPOSITE_MODE_INHERIT

Bitmaps are blended according to the mode established by the parent visual.




## -remarks



A single visual can have any combination of visual properties. However, if a 
visual has the following combination of properties, the borders of the visual will default 
to <a href="dcomposition_border_mode.htm">DCOMPOSITION_BORDER_MODE_HARD</a>.



<ul>
<li><code>SetCompositeMode(DCOMPOSITION_COMPOSITE_MODE_DESTINATION_INVERT)
</code></li>
<li><code>SetBorderMode(DCOMPOSITION_BORDER_MODE_SOFT) 
</code></li>
<li><code>SetBitmapInterpolationMode(DCOMPOSITION_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR)</code></li>
</ul>
If you want a visual to be drawn with antialiasing, use <a href="dcomposition_bitmap_interpolation_mode.htm">DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR</a> for the content of the visual, and <a href="dcomposition_border_mode.htm">DCOMPOSITION_BORDER_MODE_SOFT</a> for the edges.





## -see-also




<a href="https://msdn.microsoft.com/2F8C7930-6BBC-4CA9-86C0-168BF0F9C0BD">IDCompositionVisual::SetCompositeMode</a>
 

 

