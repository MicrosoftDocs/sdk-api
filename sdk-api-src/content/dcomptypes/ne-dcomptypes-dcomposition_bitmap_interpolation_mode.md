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

# DCOMPOSITION_BITMAP_INTERPOLATION_MODE enumeration


## -description


Specifies the interpolation mode to be used when a bitmap is composed with any transform where the pixels in the bitmap don't line up exactly one-to-one with pixels on screen. 


## -enum-fields




### -field DCOMPOSITION_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR

Bitmaps are interpolated by using nearest-neighbor sampling.


### -field DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR

Bitmaps are interpolated by using linear sampling.


### -field DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT

Bitmaps are interpolated according to the mode established by the parent visual.


## -remarks



The default interpolation mode for a visual is <b>DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT</b>. If all visuals in a visual tree specify this mode, the default for all visuals is nearest neighbor sampling, which is the fastest mode.

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
If you want a visual to be drawn with antialiasing, use <b>DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR</b> for the content of the visual, and <a href="dcomposition_border_mode.htm">DCOMPOSITION_BORDER_MODE_SOFT</a> for the edges.





## -see-also




<a href="https://msdn.microsoft.com/F45A3619-556B-4D2C-BCB0-8D55A1397579">IDCompositionVisual::SetBitmapInterpolationMode</a>
 

 

