---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

