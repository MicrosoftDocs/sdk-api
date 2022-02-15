---
UID: NE:dwrite.DWRITE_FONT_STRETCH
title: DWRITE_FONT_STRETCH (dwrite.h)
description: Represents the degree to which a font has been stretched compared to a font's normal aspect ratio.
helpviewer_keywords: ["DWRITE_FONT_STRETCH","DWRITE_FONT_STRETCH enumeration [Direct Write]","DWRITE_FONT_STRETCH_CONDENSED","DWRITE_FONT_STRETCH_EXPANDED","DWRITE_FONT_STRETCH_EXTRA_CONDENSED","DWRITE_FONT_STRETCH_EXTRA_EXPANDED","DWRITE_FONT_STRETCH_MEDIUM","DWRITE_FONT_STRETCH_NORMAL","DWRITE_FONT_STRETCH_SEMI_CONDENSED","DWRITE_FONT_STRETCH_SEMI_EXPANDED","DWRITE_FONT_STRETCH_ULTRA_CONDENSED","DWRITE_FONT_STRETCH_ULTRA_EXPANDED","DWRITE_FONT_STRETCH_UNDEFINED","directwrite.dwrite_font_stretch","dwrite/DWRITE_FONT_STRETCH","dwrite/DWRITE_FONT_STRETCH_CONDENSED","dwrite/DWRITE_FONT_STRETCH_EXPANDED","dwrite/DWRITE_FONT_STRETCH_EXTRA_CONDENSED","dwrite/DWRITE_FONT_STRETCH_EXTRA_EXPANDED","dwrite/DWRITE_FONT_STRETCH_MEDIUM","dwrite/DWRITE_FONT_STRETCH_NORMAL","dwrite/DWRITE_FONT_STRETCH_SEMI_CONDENSED","dwrite/DWRITE_FONT_STRETCH_SEMI_EXPANDED","dwrite/DWRITE_FONT_STRETCH_ULTRA_CONDENSED","dwrite/DWRITE_FONT_STRETCH_ULTRA_EXPANDED","dwrite/DWRITE_FONT_STRETCH_UNDEFINED"]
old-location: directwrite\dwrite_font_stretch.htm
tech.root: DirectWrite
ms.assetid: 10b3a703-239b-4fb1-9a20-e466b123b060
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_STRETCH, DWRITE_FONT_STRETCH enumeration [Direct Write], DWRITE_FONT_STRETCH_CONDENSED, DWRITE_FONT_STRETCH_EXPANDED, DWRITE_FONT_STRETCH_EXTRA_CONDENSED, DWRITE_FONT_STRETCH_EXTRA_EXPANDED, DWRITE_FONT_STRETCH_MEDIUM, DWRITE_FONT_STRETCH_NORMAL, DWRITE_FONT_STRETCH_SEMI_CONDENSED, DWRITE_FONT_STRETCH_SEMI_EXPANDED, DWRITE_FONT_STRETCH_ULTRA_CONDENSED, DWRITE_FONT_STRETCH_ULTRA_EXPANDED, DWRITE_FONT_STRETCH_UNDEFINED, directwrite.dwrite_font_stretch, dwrite/DWRITE_FONT_STRETCH, dwrite/DWRITE_FONT_STRETCH_CONDENSED, dwrite/DWRITE_FONT_STRETCH_EXPANDED, dwrite/DWRITE_FONT_STRETCH_EXTRA_CONDENSED, dwrite/DWRITE_FONT_STRETCH_EXTRA_EXPANDED, dwrite/DWRITE_FONT_STRETCH_MEDIUM, dwrite/DWRITE_FONT_STRETCH_NORMAL, dwrite/DWRITE_FONT_STRETCH_SEMI_CONDENSED, dwrite/DWRITE_FONT_STRETCH_SEMI_EXPANDED, dwrite/DWRITE_FONT_STRETCH_ULTRA_CONDENSED, dwrite/DWRITE_FONT_STRETCH_ULTRA_EXPANDED, dwrite/DWRITE_FONT_STRETCH_UNDEFINED
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
 - DWRITE_FONT_STRETCH
 - dwrite/DWRITE_FONT_STRETCH
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
 - DWRITE_FONT_STRETCH
---

# DWRITE_FONT_STRETCH enumeration


## -description

Represents the degree to which a font has been stretched compared to a font's normal aspect ratio.The enumerated values correspond to the <i>usWidthClass</i> definition in the OpenType specification. The usWidthClass represents an integer value between 1 and 9—lower values indicate narrower widths; higher values indicate wider widths.

## -enum-fields

### -field DWRITE_FONT_STRETCH_UNDEFINED:0

Predefined font stretch : Not known (0).

### -field DWRITE_FONT_STRETCH_ULTRA_CONDENSED:1

Predefined font stretch : Ultra-condensed (1).

### -field DWRITE_FONT_STRETCH_EXTRA_CONDENSED:2

Predefined font stretch : Extra-condensed (2).

### -field DWRITE_FONT_STRETCH_CONDENSED:3

Predefined font stretch : Condensed (3).

### -field DWRITE_FONT_STRETCH_SEMI_CONDENSED:4

Predefined font stretch : Semi-condensed (4).

### -field DWRITE_FONT_STRETCH_NORMAL:5

Predefined font stretch : Normal (5).

### -field DWRITE_FONT_STRETCH_MEDIUM:5

Predefined font stretch : Medium (5).

### -field DWRITE_FONT_STRETCH_SEMI_EXPANDED:6

Predefined font stretch : Semi-expanded (6).

### -field DWRITE_FONT_STRETCH_EXPANDED:7

Predefined font stretch : Expanded (7).

### -field DWRITE_FONT_STRETCH_EXTRA_EXPANDED:8

Predefined font stretch : Extra-expanded (8).

### -field DWRITE_FONT_STRETCH_ULTRA_EXPANDED:9

Predefined font stretch : Ultra-expanded (9).

## -remarks

A font stretch describes the degree to which a font form is stretched from its normal aspect ratio, which is the original width to height ratio specified for the glyphs in the font. 
The following illustration shows an example of Normal and Condensed stretches for the Rockwell Bold typeface.

<img alt="Illustration of “D2D” text in Normal and Condensed font stretch" src="./images/FontStretch_for_RockwellBold.png"/>

<div class="alert"><b>Note</b>  Values other than the ones defined in the enumeration are considered to be invalid, and are rejected by font API functions.</div>
<div> </div>

