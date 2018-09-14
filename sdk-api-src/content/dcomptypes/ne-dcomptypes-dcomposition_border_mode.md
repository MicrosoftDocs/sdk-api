---
UID: NE:dcomptypes.DCOMPOSITION_BORDER_MODE
title: DCOMPOSITION_BORDER_MODE
author: windows-sdk-content
description: Specifies the border mode to use when composing a bitmap or applying a clip with any transform such that the edges of the bitmap or clip are not axis-aligned with integer coordinates.
old-location: directcomp\dcomposition_border_mode.htm
tech.root: directcomp
ms.assetid: 26CDDC8A-27F5-4BE4-B345-70FF66ED5C9A
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DCOMPOSITION_BORDER_MODE, DCOMPOSITION_BORDER_MODE enumeration [DirectComposition], DCOMPOSITION_BORDER_MODE_HARD, DCOMPOSITION_BORDER_MODE_INHERIT, DCOMPOSITION_BORDER_MODE_SOFT, dcomptypes/DCOMPOSITION_BORDER_MODE, dcomptypes/DCOMPOSITION_BORDER_MODE_HARD, dcomptypes/DCOMPOSITION_BORDER_MODE_INHERIT, dcomptypes/DCOMPOSITION_BORDER_MODE_SOFT, directcomp.dcomposition_border_mode
ms.prod: windows
ms.technology: windows-sdk
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
 - DCOMPOSITION_BORDER_MODE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
If you want a visual to be drawn with antialiasing, use <a href="https://msdn.microsoft.com/en-us/library/Hh437364(v=VS.85).aspx">DCOMPOSITION_BITMAP_INTERPOLATION_MODE_LINEAR</a> for the content of the visual, and <b>DCOMPOSITION_BORDER_MODE_SOFT</b> for the edges.





## -see-also




<a href="https://msdn.microsoft.com/88C77869-B08D-43F6-8A1E-A112743C0404">IDCompositionVisual::SetBorderMode</a>
 

 

