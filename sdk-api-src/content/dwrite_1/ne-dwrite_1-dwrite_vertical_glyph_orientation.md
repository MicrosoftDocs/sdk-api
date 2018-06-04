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

# DWRITE_VERTICAL_GLYPH_ORIENTATION enumeration


## -description


The <b>DWRITE_VERTICAL_GLYPH_ORIENTATION</b> enumeration contains values that specify the desired kind of glyph orientation for the text.


## -enum-fields




### -field DWRITE_VERTICAL_GLYPH_ORIENTATION_DEFAULT

The default glyph orientation. In vertical layout, naturally horizontal scripts (Latin, Thai, Arabic, Devanagari) rotate 90 degrees clockwise, while ideographic scripts (Chinese, Japanese, Korean) remain upright, 0 degrees.


### -field DWRITE_VERTICAL_GLYPH_ORIENTATION_STACKED

Stacked glyph orientation. Ideographic scripts and scripts that permit stacking (Latin, Hebrew) are stacked in vertical reading layout. Connected scripts (Arabic, Syriac, 'Phags-pa, Ogham), which would otherwise look broken if glyphs were kept at 0 degrees, remain connected and rotate.


## -remarks



The client specifies a <b>DWRITE_VERTICAL_GLYPH_ORIENTATION</b>-typed value to the analyzer as the desired orientation.

<div class="alert"><b>Note</b>  This is the client preference, and the constraints of the script determine the final presentation.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2F229E8A-171D-4DED-9E9E-F2925855E8C0">IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation</a>
 

 

