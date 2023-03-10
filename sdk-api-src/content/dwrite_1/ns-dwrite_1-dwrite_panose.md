---
UID: NS:dwrite_1.DWRITE_PANOSE
title: DWRITE_PANOSE (dwrite_1.h)
description: The DWRITE_PANOSE union describes typeface classification values that you use with IDWriteFont1::GetPanose to select and match the font.
helpviewer_keywords: ["DWRITE_PANOSE","DWRITE_PANOSE union [Direct Write]","directwrite.dwrite_panose","dwrite_1/DWRITE_PANOSE"]
old-location: directwrite\dwrite_panose.htm
tech.root: DirectWrite
ms.assetid: B65B4C8E-1CA0-47AC-AA3F-8F2EACC5C11A
ms.date: 12/05/2018
ms.keywords: DWRITE_PANOSE, DWRITE_PANOSE union [Direct Write], directwrite.dwrite_panose, dwrite_1/DWRITE_PANOSE
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - DWRITE_PANOSE
 - dwrite_1/DWRITE_PANOSE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_PANOSE
---

## -description

The <b>DWRITE_PANOSE</b> union describes typeface classification values that you use with <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose">IDWriteFont1::GetPanose</a> to select and match the font.

## -struct-fields

### -field values

A 10-byte array of typeface classification values.

### -field familyKind

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_family">DWRITE_PANOSE_FAMILY</a>-typed value that specifies the typeface classification values to get.

### -field text

The text structure.

### -field text.familyKind

The <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_family">DWRITE_PANOSE_FAMILY_TEXT_DISPLAY</a> value (2) that specifies text display typeface classification.

### -field text.serifStyle

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_serif_style">DWRITE_PANOSE_SERIF_STYLE</a>-typed value that specifies the serif style of text.

### -field text.weight

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_weight">DWRITE_PANOSE_WEIGHT</a>-typed value that specifies the weight of the text.

### -field text.proportion

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_proportion">DWRITE_PANOSE_PROPORTION</a>-typed value that specifies the proportion for the text.

### -field text.contrast

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_contrast">DWRITE_PANOSE_CONTRAST</a>-typed value that specifies the contrast for the text.

### -field text.strokeVariation

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation">DWRITE_PANOSE_STROKE_VARIATION</a>-typed value that specifies the stroke variation for the text.

### -field text.armStyle

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_arm_style">DWRITE_PANOSE_ARM_STYLE</a>-typed value that specifies the arm style of text.

### -field text.letterform

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_letterform">DWRITE_PANOSE_LETTERFORM</a>-typed value that specifies the letter form for the text.

### -field text.midline

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_midline">DWRITE_PANOSE_MIDLINE</a>-typed value that specifies the midline for the text.

### -field text.xHeight

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_xheight">DWRITE_PANOSE_XHEIGHT</a>-typed value that specifies the relative size of lowercase text.

### -field script

The script structure.

### -field script.familyKind

The <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_family">DWRITE_PANOSE_FAMILY_SCRIPT</a> value (3) that specifies script typeface classification.

### -field script.toolKind

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind">DWRITE_PANOSE_TOOL_KIND</a>-typed value that specifies the kind of tool for the script.

### -field script.weight

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_weight">DWRITE_PANOSE_WEIGHT</a>-typed value that specifies the weight of the script.

### -field script.spacing

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_spacing">DWRITE_PANOSE_SPACING</a>-typed value that specifies the spacing of the script.

### -field script.aspectRatio

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio">DWRITE_PANOSE_ASPECT_RATIO</a>-typed value that specifies the aspect ratio of the script.

### -field script.contrast

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_contrast">DWRITE_PANOSE_CONTRAST</a>-typed value that specifies the contrast for the script.

### -field script.scriptTopology

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_script_topology">DWRITE_PANOSE_SCRIPT_TOPOLOGY</a>-typed value that specifies the script topology.

### -field script.scriptForm

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_script_form">DWRITE_PANOSE_SCRIPT_FORM</a>-typed value that specifies the script form.

### -field script.finials

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_finials">DWRITE_PANOSE_FINIALS</a>-typed value that specifies the script finials.

### -field script.xAscent

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_xascent">DWRITE_PANOSE_XASCENT</a>-typed value that specifies the relative size of lowercase letters.

### -field decorative

The decorative structure.

### -field decorative.familyKind

The <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_family">DWRITE_PANOSE_FAMILY_DECORATIVE</a> value (4) that specifies decorative typeface classification.

### -field decorative.decorativeClass

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class">DWRITE_PANOSE_DECORATIVE_CLASS</a>-typed value that specifies the class of the decorative typeface.

### -field decorative.weight

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_weight">DWRITE_PANOSE_WEIGHT</a>-typed value that specifies the weight of the decorative typeface.

### -field decorative.aspect

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_aspect">DWRITE_PANOSE_ASPECT</a>-typed value that specifies the aspect of the decorative typeface.

### -field decorative.contrast

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_contrast">DWRITE_PANOSE_CONTRAST</a>-typed value that specifies the contrast for the decorative typeface.

### -field decorative.serifVariant

The serif variant of the decorative typeface.

### -field decorative.fill

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_fill">DWRITE_PANOSE_FILL</a>-typed value that specifies the fill of the decorative typeface.

### -field decorative.lining

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_lining">DWRITE_PANOSE_LINING</a>-typed value that specifies the lining of the decorative typeface.

### -field decorative.decorativeTopology

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology">DWRITE_PANOSE_DECORATIVE_TOPOLOGY</a>-typed value that specifies the decorative topology.

### -field decorative.characterRange

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges">DWRITE_PANOSE_CHARACTER_RANGES</a>-typed value that specifies the character range of the decorative typeface.

### -field symbol

The symbol structure.

### -field symbol.familyKind

The <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_family">DWRITE_PANOSE_FAMILY_SYMBOL</a> value (5) that specifies symbol typeface classification.

### -field symbol.symbolKind

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind">DWRITE_PANOSE_SYMBOL_KIND</a>-typed value that specifies the kind of symbol set.

### -field symbol.weight

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_weight">DWRITE_PANOSE_WEIGHT</a>-typed value that specifies the weight of the symbol typeface.

### -field symbol.spacing

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_spacing">DWRITE_PANOSE_SPACING</a>-typed value that specifies the spacing of the symbol typeface.

### -field symbol.aspectRatioAndContrast

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio and contrast of the symbol typeface.

### -field symbol.aspectRatio94

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 94 of the symbol typeface.

### -field symbol.aspectRatio119

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 119 of the symbol typeface.

### -field symbol.aspectRatio157

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 157 of the symbol typeface.

### -field symbol.aspectRatio163

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 163 of the symbol typeface.

### -field symbol.aspectRatio211

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio">DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</a>-typed value that specifies the aspect ratio 211 of the symbol typeface.

## -remarks

<div class="alert"><b>Note</b>  The <b>familyKind</b> member (index 0) is the only stable entry in the 10-byte array because all the entries that follow can change dynamically depending on the context of the first member.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_panose_family">DWRITE_PANOSE_FAMILY</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose">IDWriteFont1::GetPanose</a>

