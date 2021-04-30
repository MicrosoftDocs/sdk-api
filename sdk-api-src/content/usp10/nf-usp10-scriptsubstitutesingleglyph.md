---
UID: NF:usp10.ScriptSubstituteSingleGlyph
title: ScriptSubstituteSingleGlyph function (usp10.h)
description: Enables substitution of a single glyph with one alternate form of the same glyph for OpenType processing.
helpviewer_keywords: ["ScriptSubstituteSingleGlyph","ScriptSubstituteSingleGlyph function [Internationalization for Windows Applications]","_win32_ScriptSubstituteSingleGlyph","intl.scriptsubstitutesingleglyph","usp10/ScriptSubstituteSingleGlyph"]
old-location: intl\scriptsubstitutesingleglyph.htm
tech.root: Intl
ms.assetid: 1aecde5a-ddca-4163-9159-dafc15f9ca59
ms.date: 12/05/2018
ms.keywords: ScriptSubstituteSingleGlyph, ScriptSubstituteSingleGlyph function [Internationalization for Windows Applications], _win32_ScriptSubstituteSingleGlyph, intl.scriptsubstitutesingleglyph, usp10/ScriptSubstituteSingleGlyph
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
 - ScriptSubstituteSingleGlyph
 - usp10/ScriptSubstituteSingleGlyph
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptSubstituteSingleGlyph
---

# ScriptSubstituteSingleGlyph function


## -description

Enables substitution of a single glyph with one alternate form of the same glyph for OpenType processing.

## -parameters

### -param hdc [in, optional]

Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure indicating the script cache.

### -param psa [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>. This parameter identifies the shaping engine so that the correct substitute glyph is used.

Alternatively, the application can set this parameter to <b>NULL</b> to retrieve unfiltered results.

### -param tagScript [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure defining the script tag for shaping.

### -param tagLangSys [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure defining the language tag for shaping.

### -param tagFeature [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure defining the feature tag to use for shaping the alternate glyph.

### -param lParameter [in]

Reference to the alternate glyph to substitute. This reference is an index to an array that contains all the alternate glyphs defined in the feature, as illustrated for <a href="/windows/desktop/api/usp10/ns-usp10-opentype_feature_record">OPENTYPE_FEATURE_RECORD</a>. The alternate glyph array is one of the items retrieved by <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetfontalternateglyphs">ScriptGetFontAlternateGlyphs</a>.

### -param wGlyphId [in]

Identifier of the original glyph.

### -param pwOutGlyphId [out]

Pointer to the location in which this function retrieves the identifier of the alternate glyph.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

This function uses one-to-one substitution in which the application can substitute one glyph with one alternate form. Most often, applications use this function to set a bullet or an alternate glyph at the beginning or end of a line.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/caching">Caching</a>



<a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptgetfontalternateglyphs">ScriptGetFontAlternateGlyphs</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>