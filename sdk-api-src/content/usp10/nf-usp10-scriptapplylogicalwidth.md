---
UID: NF:usp10.ScriptApplyLogicalWidth
title: ScriptApplyLogicalWidth function (usp10.h)
description: Takes an array of advance widths for a run and generates an array of adjusted advance glyph widths.
helpviewer_keywords: ["ScriptApplyLogicalWidth","ScriptApplyLogicalWidth function [Internationalization for Windows Applications]","_win32_ScriptApplyLogicalWidth","intl.scriptapplylogicalwidth","usp10/ScriptApplyLogicalWidth"]
old-location: intl\scriptapplylogicalwidth.htm
tech.root: Intl
ms.assetid: 964634f4-700b-47a7-a86f-071f1c97bcbe
ms.date: 12/05/2018
ms.keywords: ScriptApplyLogicalWidth, ScriptApplyLogicalWidth function [Internationalization for Windows Applications], _win32_ScriptApplyLogicalWidth, intl.scriptapplylogicalwidth, usp10/ScriptApplyLogicalWidth
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
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
f1_keywords:
 - ScriptApplyLogicalWidth
 - usp10/ScriptApplyLogicalWidth
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptApplyLogicalWidth
---

# ScriptApplyLogicalWidth function


## -description

Takes an array of advance widths for a <a href="/windows/desktop/Intl/uniscribe-glossary">run</a> and generates an array of adjusted advance glyph widths.

## -parameters

### -param piDx [in]

Pointer to an array of <a href="/windows/desktop/Intl/uniscribe-glossary">advance widths</a> in logical order, one per code point.

### -param cChars [in]

Count of the logical code points in the run.

### -param cGlyphs [in]

Glyph count.

### -param pwLogClust [in]

Pointer to an array of logical clusters from <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>.

### -param psva [in]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a> structure from <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a> and updated by <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>.

### -param piAdvance [in]

Pointer to an array of glyph advance widths from <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>.

### -param psa [in]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure from <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a> and updated by <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a> and <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>.

### -param pABC [in, out, optional]

Pointer to the overall <a href="/windows/desktop/Intl/uniscribe-glossary">ABC width</a> of a run. On input, the parameter should contain the run ABC widths retrieved by <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>. On output, the parameter indicates the ABC width updated to match the new widths.

### -param piJustify [out]

Pointer to an array in which the function retrieves the glyph advance widths. This array is suitable for passing to the <i>piJustify</i> parameter of <a href="/windows/desktop/api/usp10/nf-usp10-scripttextout">ScriptTextOut</a>.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

This function can be used to reapply logical widths obtained with <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetlogicalwidths">ScriptGetLogicalWidths</a>. It can be useful in situations such as metafiling, for which advance width information must be recorded and reapplied in a font-independent manner, independent of glyph substitutions, such as ligaturization.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptgetlogicalwidths">ScriptGetLogicalWidths</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scripttextout">ScriptTextOut</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>