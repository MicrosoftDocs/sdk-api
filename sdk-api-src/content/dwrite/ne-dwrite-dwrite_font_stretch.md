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

# DWRITE_FONT_STRETCH enumeration


## -description


Represents the degree to which a font has been stretched compared to a font's normal aspect ratio.
  The enumerated values correspond to the <i>usWidthClass</i> definition in the OpenType specification. The usWidthClass represents an integer value between 1 and 9—lower values indicate narrower widths; higher values indicate wider widths.


## -enum-fields




### -field DWRITE_FONT_STRETCH_UNDEFINED

Predefined font stretch : Not known (0).


### -field DWRITE_FONT_STRETCH_ULTRA_CONDENSED

Predefined font stretch : Ultra-condensed (1).


### -field DWRITE_FONT_STRETCH_EXTRA_CONDENSED

Predefined font stretch : Extra-condensed (2).


### -field DWRITE_FONT_STRETCH_CONDENSED

Predefined font stretch : Condensed (3).


### -field DWRITE_FONT_STRETCH_SEMI_CONDENSED

Predefined font stretch : Semi-condensed (4).


### -field DWRITE_FONT_STRETCH_NORMAL

Predefined font stretch : Normal (5).


### -field DWRITE_FONT_STRETCH_MEDIUM

Predefined font stretch : Medium (5).


### -field DWRITE_FONT_STRETCH_SEMI_EXPANDED

Predefined font stretch : Semi-expanded (6).


### -field DWRITE_FONT_STRETCH_EXPANDED

Predefined font stretch : Expanded (7).


### -field DWRITE_FONT_STRETCH_EXTRA_EXPANDED

Predefined font stretch : Extra-expanded (8).


### -field DWRITE_FONT_STRETCH_ULTRA_EXPANDED

Predefined font stretch : Ultra-expanded (9).


## -remarks



A font stretch describes the degree to which a font form is stretched from its normal aspect ratio, which is the original width to height ratio specified for the glyphs in the font. 
The following illustration shows an example of Normal and Condensed stretches for the Rockwell Bold typeface.

<img alt="Illustration of “D2D” text in Normal and Condensed font stretch" src="images/FontStretch_for_RockwellBold.png"/>

<div class="alert"><b>Note</b>  Values other than the ones defined in the enumeration are considered to be invalid, and are rejected by font API functions.</div>
<div> </div>


