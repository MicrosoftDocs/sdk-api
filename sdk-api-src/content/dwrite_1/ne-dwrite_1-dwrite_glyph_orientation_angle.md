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

# DWRITE_GLYPH_ORIENTATION_ANGLE enumeration


## -description


The <b>DWRITE_GLYPH_ORIENTATION_ANGLE</b> enumeration contains values that specify how the glyph is oriented to the x-axis.


## -enum-fields




### -field DWRITE_GLYPH_ORIENTATION_ANGLE_0_DEGREES

Glyph orientation is upright.


### -field DWRITE_GLYPH_ORIENTATION_ANGLE_90_DEGREES

Glyph orientation is rotated 90 degrees clockwise.


### -field DWRITE_GLYPH_ORIENTATION_ANGLE_180_DEGREES

Glyph orientation is upside-down.


### -field DWRITE_GLYPH_ORIENTATION_ANGLE_270_DEGREES

Glyph orientation is rotated 270 degrees clockwise.


## -remarks



The text analyzer outputs <b>DWRITE_GLYPH_ORIENTATION_ANGLE</b> values. The value that it outputs depends on the desired orientation, bidi level, and character properties.




## -see-also




<a href="https://msdn.microsoft.com/81BD4C36-273B-4C28-A89E-88BABCAD511A">IDWriteTextAnalysisSink1::SetGlyphOrientation</a>



<a href="https://msdn.microsoft.com/583AFE54-F816-4098-844B-C3F838BE46B0">IDWriteTextAnalyzer1::GetGlyphOrientationTransform</a>
 

 

