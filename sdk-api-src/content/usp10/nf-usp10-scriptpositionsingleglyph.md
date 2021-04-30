---
UID: NF:usp10.ScriptPositionSingleGlyph
title: ScriptPositionSingleGlyph function (usp10.h)
description: Positions a single glyph with a single adjustment using a specified feature provided in the font for OpenType processing. Most often, applications use this function to align a glyph optically at the beginning or end of a line.
helpviewer_keywords: ["ScriptPositionSingleGlyph","ScriptPositionSingleGlyph function [Internationalization for Windows Applications]","_win32_ScriptPositionSingleGlyph","intl.scriptpositionsingleglyph","usp10/ScriptPositionSingleGlyph"]
old-location: intl\scriptpositionsingleglyph.htm
tech.root: Intl
ms.assetid: 8dc776a9-fdde-4982-a2ca-e4384615bc47
ms.date: 12/05/2018
ms.keywords: ScriptPositionSingleGlyph, ScriptPositionSingleGlyph function [Internationalization for Windows Applications], _win32_ScriptPositionSingleGlyph, intl.scriptpositionsingleglyph, usp10/ScriptPositionSingleGlyph
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Usp10.dll version 1.600 or greater on Windows XP
ms.custom: 19H1
f1_keywords:
 - ScriptPositionSingleGlyph
 - usp10/ScriptPositionSingleGlyph
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptPositionSingleGlyph
---

# ScriptPositionSingleGlyph function


## -description

Positions a single glyph with a single adjustment using a specified feature provided in the font for OpenType processing. Most often, applications use this function to align a glyph optically at the beginning or end of a line.

## -parameters

### -param hdc [in, optional]

Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param psa [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>. This structure identifies the shaping engine, so that the advance widths can be retrieved.

Alternatively, the application can set this parameter to <b>NULL</b> to retrieve unfiltered results.

### -param tagScript [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure defining the script tag for shaping.

### -param tagLangSys [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure defining the language tag for shaping.

### -param tagFeature [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure defining the feature tag to use for shaping the alternate glyph.

### -param lParameter [in]

A flag specifying if single substitution should be applied to the identifier specified in <i>wGlyphId</i>. The application sets this parameter to 1 to apply the single substitution feature to the identifier. The application sets the parameter to 0 if the function should not apply the feature.

### -param wGlyphId [in]

The identifier of the original glyph being shaped.

### -param iAdvance [in]

The original glyph advance width.

### -param GOffset [in]

The original glyph offset. Typically, this value is an output of <a href="/windows/desktop/api/usp10/nf-usp10-scriptplaceopentype">ScriptPlaceOpenType</a> or <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>.

### -param piOutAdvance [out]

Pointer to the location in which this function retrieves the new advance width adjusted for the alternate glyph.

### -param pOutGoffset [out]

Pointer to the location in which this function retrieves the new glyph offset adjusted for the alternate glyph.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

This function positions an individual glyph by adjusting the advance width and/or the offset of the given glyph. The function assumes that the font requires only one adjustment.

A typical use of this function is the slight adjustment of the margin to account for the visual impression made by certain characters. In Latin script, for example, at the beginning of a line it is common to make a slight adjustment to the left for an initial capital (such as "T" or "O") that does not have a vertical line on the left part of the glyph. Although doing this breaks the strict linear margin, the eye perceives the margin as more even.

The following examples demonstrate this effect. The first example shows strict alignment; the next two examples show an adjustment of the initial "T" to the left. The adjustments are by one pixel and two pixels, respectively. The magnified images to the right show how the "T" pushes slightly farther into the left margin in each successive case.

<img alt="Illustration showing the same block of text three times, with enlargements of each showing slightly different alignment" border="" src="./images/HAlign.gif"/>
<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/caching">Caching</a>



<a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>