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

# DCOMPOSITION_BORDER_MODE enumeration


## -description


Specifies the border mode to use when composing a bitmap or applying a clip with any transform such that the edges of the bitmap or clip are not axis-aligned with integer coordinates. 


## -enum-fields




### -field DCOMPOSITION_BORDER_MODE_SOFT

Bitmap and clip edges are antialiased.


### -field DCOMPOSITION_BORDER_MODE_HARD

Bitmap and clip edges are aliased. See Remarks.


### -field DCOMPOSITION_BORDER_MODE_INHERIT

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
If you want a visual to be drawn with antialiasing, use <a href="dcomposition_bitmap_interpolation_mode.htm">DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR</a> for the content of the visual, and <b>DCOMPOSITION_BORDER_MODE_SOFT</b> for the edges.





## -see-also




<a href="https://msdn.microsoft.com/88C77869-B08D-43F6-8A1E-A112743C0404">IDCompositionVisual::SetBorderMode</a>
 

 

