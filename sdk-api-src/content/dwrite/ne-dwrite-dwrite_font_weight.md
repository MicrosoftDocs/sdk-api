---
UID: NE:dwrite.DWRITE_FONT_WEIGHT
title: DWRITE_FONT_WEIGHT (dwrite.h)
description: Represents the density of a typeface, in terms of the lightness or heaviness of the strokes.
helpviewer_keywords: ["DWRITE_FONT_WEIGHT","DWRITE_FONT_WEIGHT enumeration [Direct Write]","DWRITE_FONT_WEIGHT_BLACK","DWRITE_FONT_WEIGHT_BOLD","DWRITE_FONT_WEIGHT_DEMI_BOLD","DWRITE_FONT_WEIGHT_EXTRA_BLACK","DWRITE_FONT_WEIGHT_EXTRA_BOLD","DWRITE_FONT_WEIGHT_EXTRA_LIGHT","DWRITE_FONT_WEIGHT_HEAVY","DWRITE_FONT_WEIGHT_LIGHT","DWRITE_FONT_WEIGHT_MEDIUM","DWRITE_FONT_WEIGHT_NORMAL","DWRITE_FONT_WEIGHT_REGULAR","DWRITE_FONT_WEIGHT_SEMI_BOLD","DWRITE_FONT_WEIGHT_SEMI_LIGHT","DWRITE_FONT_WEIGHT_THIN","DWRITE_FONT_WEIGHT_ULTRA_BLACK","DWRITE_FONT_WEIGHT_ULTRA_BOLD","DWRITE_FONT_WEIGHT_ULTRA_LIGHT","directwrite.dwrite_font_weight","dwrite/DWRITE_FONT_WEIGHT","dwrite/DWRITE_FONT_WEIGHT_BLACK","dwrite/DWRITE_FONT_WEIGHT_BOLD","dwrite/DWRITE_FONT_WEIGHT_DEMI_BOLD","dwrite/DWRITE_FONT_WEIGHT_EXTRA_BLACK","dwrite/DWRITE_FONT_WEIGHT_EXTRA_BOLD","dwrite/DWRITE_FONT_WEIGHT_EXTRA_LIGHT","dwrite/DWRITE_FONT_WEIGHT_HEAVY","dwrite/DWRITE_FONT_WEIGHT_LIGHT","dwrite/DWRITE_FONT_WEIGHT_MEDIUM","dwrite/DWRITE_FONT_WEIGHT_NORMAL","dwrite/DWRITE_FONT_WEIGHT_REGULAR","dwrite/DWRITE_FONT_WEIGHT_SEMI_BOLD","dwrite/DWRITE_FONT_WEIGHT_SEMI_LIGHT","dwrite/DWRITE_FONT_WEIGHT_THIN","dwrite/DWRITE_FONT_WEIGHT_ULTRA_BLACK","dwrite/DWRITE_FONT_WEIGHT_ULTRA_BOLD","dwrite/DWRITE_FONT_WEIGHT_ULTRA_LIGHT"]
old-location: directwrite\dwrite_font_weight.htm
tech.root: DirectWrite
ms.assetid: 82396f80-eb62-4865-ba07-9653220c84f2
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_WEIGHT, DWRITE_FONT_WEIGHT enumeration [Direct Write], DWRITE_FONT_WEIGHT_BLACK, DWRITE_FONT_WEIGHT_BOLD, DWRITE_FONT_WEIGHT_DEMI_BOLD, DWRITE_FONT_WEIGHT_EXTRA_BLACK, DWRITE_FONT_WEIGHT_EXTRA_BOLD, DWRITE_FONT_WEIGHT_EXTRA_LIGHT, DWRITE_FONT_WEIGHT_HEAVY, DWRITE_FONT_WEIGHT_LIGHT, DWRITE_FONT_WEIGHT_MEDIUM, DWRITE_FONT_WEIGHT_NORMAL, DWRITE_FONT_WEIGHT_REGULAR, DWRITE_FONT_WEIGHT_SEMI_BOLD, DWRITE_FONT_WEIGHT_SEMI_LIGHT, DWRITE_FONT_WEIGHT_THIN, DWRITE_FONT_WEIGHT_ULTRA_BLACK, DWRITE_FONT_WEIGHT_ULTRA_BOLD, DWRITE_FONT_WEIGHT_ULTRA_LIGHT, directwrite.dwrite_font_weight, dwrite/DWRITE_FONT_WEIGHT, dwrite/DWRITE_FONT_WEIGHT_BLACK, dwrite/DWRITE_FONT_WEIGHT_BOLD, dwrite/DWRITE_FONT_WEIGHT_DEMI_BOLD, dwrite/DWRITE_FONT_WEIGHT_EXTRA_BLACK, dwrite/DWRITE_FONT_WEIGHT_EXTRA_BOLD, dwrite/DWRITE_FONT_WEIGHT_EXTRA_LIGHT, dwrite/DWRITE_FONT_WEIGHT_HEAVY, dwrite/DWRITE_FONT_WEIGHT_LIGHT, dwrite/DWRITE_FONT_WEIGHT_MEDIUM, dwrite/DWRITE_FONT_WEIGHT_NORMAL, dwrite/DWRITE_FONT_WEIGHT_REGULAR, dwrite/DWRITE_FONT_WEIGHT_SEMI_BOLD, dwrite/DWRITE_FONT_WEIGHT_SEMI_LIGHT, dwrite/DWRITE_FONT_WEIGHT_THIN, dwrite/DWRITE_FONT_WEIGHT_ULTRA_BLACK, dwrite/DWRITE_FONT_WEIGHT_ULTRA_BOLD, dwrite/DWRITE_FONT_WEIGHT_ULTRA_LIGHT
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_FONT_WEIGHT
 - dwrite/DWRITE_FONT_WEIGHT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_FONT_WEIGHT
---

# DWRITE_FONT_WEIGHT enumeration


## -description

Represents the density of a typeface, in terms of the lightness or heaviness of the strokes. The enumerated values correspond to the usWeightClass definition in the OpenType specification. The <i>usWeightClass</i> represents an integer value between 1 and 999. Lower values indicate lighter weights; higher values indicate heavier weights.

## -enum-fields

### -field DWRITE_FONT_WEIGHT_THIN:100

Predefined font weight : Thin (100).

### -field DWRITE_FONT_WEIGHT_EXTRA_LIGHT:200

Predefined font weight : Extra-light (200).

### -field DWRITE_FONT_WEIGHT_ULTRA_LIGHT:200

Predefined font weight : Ultra-light (200).

### -field DWRITE_FONT_WEIGHT_LIGHT:300

Predefined font weight : Light (300).

### -field DWRITE_FONT_WEIGHT_SEMI_LIGHT:350

Predefined font weight : Semi-Light (350).

### -field DWRITE_FONT_WEIGHT_NORMAL:400

Predefined font weight : Normal (400).

### -field DWRITE_FONT_WEIGHT_REGULAR:400

Predefined font weight : Regular (400).

### -field DWRITE_FONT_WEIGHT_MEDIUM:500

Predefined font weight : Medium (500).

### -field DWRITE_FONT_WEIGHT_DEMI_BOLD:600

Predefined font weight : Demi-bold (600).

### -field DWRITE_FONT_WEIGHT_SEMI_BOLD:600

Predefined font weight : Semi-bold (600).

### -field DWRITE_FONT_WEIGHT_BOLD:700

Predefined font weight : Bold (700).

### -field DWRITE_FONT_WEIGHT_EXTRA_BOLD:800

Predefined font weight : Extra-bold (800).

### -field DWRITE_FONT_WEIGHT_ULTRA_BOLD:800

Predefined font weight : Ultra-bold (800).

### -field DWRITE_FONT_WEIGHT_BLACK:900

Predefined font weight : Black (900).

### -field DWRITE_FONT_WEIGHT_HEAVY:900

Predefined font weight : Heavy (900).

### -field DWRITE_FONT_WEIGHT_EXTRA_BLACK:950

Predefined font weight : Extra-black (950).

### -field DWRITE_FONT_WEIGHT_ULTRA_BLACK:950

Predefined font weight : Ultra-black (950).

## -remarks

Weight differences are generally differentiated by an increased stroke or thickness that is associated with a given character in a typeface, as compared to a "normal" character from that same typeface. 
The following illustration shows an example of Normal and UltraBold weights for the Palatino Linotype typeface.

<img alt='Illustration of the letter "W" in Normal and UltraBold weights' src="./images/FontWeight_for_Palatino.png"/>

<div class="alert"><b>Note</b>  Not all weights are available for all typefaces. When a weight is not available for a typeface, the closest matching weight is returned.</div>
<div> </div>
Font weight values less than 1 or greater than 999 are considered invalid, and they are rejected by font API functions.

