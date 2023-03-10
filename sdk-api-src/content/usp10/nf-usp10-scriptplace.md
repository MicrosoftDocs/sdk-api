---
UID: NF:usp10.ScriptPlace
title: ScriptPlace function (usp10.h)
description: Generates glyph advance width and two-dimensional offset information from the output of ScriptShape.
helpviewer_keywords: ["ScriptPlace","ScriptPlace function [Internationalization for Windows Applications]","_win32_ScriptPlace","intl.scriptplace","usp10/ScriptPlace"]
old-location: intl\scriptplace.htm
tech.root: Intl
ms.assetid: 7f88432f-052f-4781-8346-31c8a0771e51
ms.date: 12/05/2018
ms.keywords: ScriptPlace, ScriptPlace function [Internationalization for Windows Applications], _win32_ScriptPlace, intl.scriptplace, usp10/ScriptPlace
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ScriptPlace
 - usp10/ScriptPlace
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
 - ScriptPlace
---

# ScriptPlace function


## -description

Generates glyph <a href="/windows/desktop/Intl/uniscribe-glossary">advance width</a> and two-dimensional offset information from the output of <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>.

## -parameters

### -param hdc [in]

Optional. Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param pwGlyphs [in]

Pointer to a glyph buffer obtained from an earlier call to the <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a> function.

### -param cGlyphs [in]

Count of glyphs in the glyph buffer.

### -param psva [in]

Pointer to an array of <a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a> structures indicating visual attributes.

### -param psa [in, out]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure. On input, this structure is obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>. On output, this structure contains values retrieved by <b>ScriptPlace</b>.

### -param piAdvance [out]

Pointer to an array in which this function retrieves advance width information.

### -param pGoffset [out]

Optional. Pointer to an array of <a href="/windows/desktop/api/usp10/ns-usp10-goffset">GOFFSET</a> structures in which this function retrieves the x and y offsets of combining glyphs. This array must be of length indicated by <i>cGlyphs</i>.

### -param pABC [out]

Pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-abc">ABC</a> structure in which this function retrieves the <a href="/windows/desktop/Intl/uniscribe-glossary">ABC width</a> for the entire <a href="/windows/desktop/Intl/uniscribe-glossary">run</a>.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

The function returns E_PENDING if the script cache specified by the <i>psc</i> parameter does not contain enough information to place the glyphs, and the <i>hdc</i> parameter is set to <b>NULL</b> so that the function cannot complete the placement process. The application should set up a correct device context for the run, and call this function again with the appropriate device context and with all other parameters the same.

## -remarks

See <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

The composite ABC width for the whole item identifies how much the glyphs <a href="/windows/desktop/Intl/uniscribe-glossary">overhang</a> to the left of the start position and to the right of the length implied by the sum of the advance widths. The total advance width of the line is exactly abcA+abcB+abcC. The abcA and abcC values are maintained as proportions of the cell height represented in 8 bits and are thus roughly +/-1 percent. The total width retrieved, which is the sum of the abcA+abcB+abcC values indicated by <i>piAdvance</i>, is accurate to the resolution of the TrueType shaping engine.

All arrays are in visual order unless the <b>fLogicalOrder</b> member is set in the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure indicated by the <i>psa</i> parameter.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/desktop/api/usp10/ns-usp10-goffset">GOFFSET</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplaceopentype">ScriptPlaceOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>