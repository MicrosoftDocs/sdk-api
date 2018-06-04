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

# DWRITE_FONT_WEIGHT enumeration


## -description


Represents the density of a typeface, in terms of the lightness or heaviness of the strokes. The enumerated values correspond to the usWeightClass definition in the OpenType specification. The <i>usWeightClass</i> represents an integer value between 1 and 999. Lower values indicate lighter weights; higher values indicate heavier weights.


## -enum-fields




### -field DWRITE_FONT_WEIGHT_THIN

Predefined font weight : Thin (100).


### -field DWRITE_FONT_WEIGHT_EXTRA_LIGHT

Predefined font weight : Extra-light (200).


### -field DWRITE_FONT_WEIGHT_ULTRA_LIGHT

Predefined font weight : Ultra-light (200).


### -field DWRITE_FONT_WEIGHT_LIGHT

Predefined font weight : Light (300).


### -field DWRITE_FONT_WEIGHT_SEMI_LIGHT

Predefined font weight : Semi-Light (350).


### -field DWRITE_FONT_WEIGHT_NORMAL

Predefined font weight : Normal (400).


### -field DWRITE_FONT_WEIGHT_REGULAR

Predefined font weight : Regular (400).


### -field DWRITE_FONT_WEIGHT_MEDIUM

Predefined font weight : Medium (500).


### -field DWRITE_FONT_WEIGHT_DEMI_BOLD

Predefined font weight : Demi-bold (600).


### -field DWRITE_FONT_WEIGHT_SEMI_BOLD

Predefined font weight : Semi-bold (600).


### -field DWRITE_FONT_WEIGHT_BOLD

Predefined font weight : Bold (700).


### -field DWRITE_FONT_WEIGHT_EXTRA_BOLD

Predefined font weight : Extra-bold (800).


### -field DWRITE_FONT_WEIGHT_ULTRA_BOLD

Predefined font weight : Ultra-bold (800).


### -field DWRITE_FONT_WEIGHT_BLACK

Predefined font weight : Black (900).


### -field DWRITE_FONT_WEIGHT_HEAVY

Predefined font weight : Heavy (900).


### -field DWRITE_FONT_WEIGHT_EXTRA_BLACK

Predefined font weight : Extra-black (950).


### -field DWRITE_FONT_WEIGHT_ULTRA_BLACK

Predefined font weight : Ultra-black (950).


## -remarks



Weight differences are generally differentiated by an increased stroke or thickness that is associated with a given character in a typeface, as compared to a "normal" character from that same typeface. 
The following illustration shows an example of Normal and UltraBold weights for the Palatino Linotype typeface.

<img alt='Illustration of the letter "W" in Normal and UltraBold weights' src="images/FontWeight_for_Palatino.png"/>

<div class="alert"><b>Note</b>  Not all weights are available for all typefaces. When a weight is not available for a typeface, the closest matching weight is returned.</div>
<div> </div>
Font weight values less than 1 or greater than 999 are considered invalid, and they are rejected by font API functions.



