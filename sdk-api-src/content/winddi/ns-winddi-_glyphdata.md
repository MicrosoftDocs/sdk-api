---
UID: NS:winddi._GLYPHDATA
title: "_GLYPHDATA"
author: windows-sdk-content
description: The GLYPHDATA structure contains information about an individual glyph.
old-location: display\glyphdata.htm
old-project: display
ms.assetid: 9153b8c7-e6ad-4297-a0b6-ea495b9b312f
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: GLYPHDATA, GLYPHDATA structure [Display Devices], _GLYPHDATA, display.glyphdata, grstrcts_e96122df-3f9d-4e90-9bf6-25017381e514.xml, winddi/GLYPHDATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: GLYPHDATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - GLYPHDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _GLYPHDATA structure


## -description


The GLYPHDATA structure contains information about an individual glyph.


## -struct-fields




### -field gdf

Specifies a <a href="https://msdn.microsoft.com/d1a7a02c-acaf-46b5-9ffe-fddbb01408a5">GLYPHDEF</a> union that contains a pointer to either a <a href="https://msdn.microsoft.com/d7e0b5dd-dd94-4fc2-8c90-0d656a84c46b">GLYPHBITS</a> structure or a <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure, depending on whether, respectively, the glyph data is in the form of a bitmap or an outline.


### -field hg

Handle to the glyph.


### -field fxD

Specifies a FIX value containing the character increment amount, D = A + B + C. The character increment amount represents the sum of the prebearing, or left sidebearing amount (A), the width of the glyph (B), and the width of the right sidebearing amount (C). The two sidebearing amounts represent the (usually) empty space immediately to the left and right of the glyph. The value stored in <b>fxD</b> is the dot product of D and a unit vector along the baseline (in device coordinates), yielding the projection of D onto the baseline. 


### -field fxA

Specifies a FIX value containing the prebearing, or left sidebearing amount, A. The value stored in <b>fxA</b> is the dot product of A and a unit vector along the baseline (in device coordinates), yielding the projection of A onto the baseline.


### -field fxAB

Specifies a FIX value containing the advancing edge of the character, A + B. The value stored in fxAB is the dot product of A + B and a unit vector along the baseline (in device coordinates), yielding the projection of A + B onto the baseline.


### -field fxInkTop

Specifies a FIX value containing the distance between the baseline and the ink box top along a unit vector in the ascent direction (in device coordinates).


### -field fxInkBottom

Specifies a FIX value containing the distance between the baseline and the ink box bottom along a unit vector in the ascent direction (in device coordinates).


### -field rclInk

Specifies a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that describes the ink box in which the glyph fits. The sides of the ink box are parallel to the x and y axes.


### -field ptqD

Specifies a POINTQF structure that contains the character increment vector, D = A + B + C. The high-order WORDs of <b>ptqD</b> are 28.4 device coordinates. The low-order WORDs of this member provide additional precision. For a description of the POINTQF structure, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


## -remarks



The quantities A, B, and C mentioned in the descriptions of GLYPHDATA members are simple tranforms of the notional space versions into 28.4 device coordinates. A is the left sidebearing amount, the width of the space to the left of the glyph, B is the width of the glyph, and C is the right sidebearing amount, the width of the space to the right of the glyph. For some glyphs, A and/or C can be negative, indicating that the glyph extends farther to the left and/or right than is usually the case.

For a description of the FIX data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.




## -see-also




<a href="https://msdn.microsoft.com/d7e0b5dd-dd94-4fc2-8c90-0d656a84c46b">GLYPHBITS</a>



<a href="https://msdn.microsoft.com/d1a7a02c-acaf-46b5-9ffe-fddbb01408a5">GLYPHDEF</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>
 

 

