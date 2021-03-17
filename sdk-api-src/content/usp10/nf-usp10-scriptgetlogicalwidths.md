---
UID: NF:usp10.ScriptGetLogicalWidths
title: ScriptGetLogicalWidths function (usp10.h)
description: Converts the glyph advance widths for a specific font into logical widths.
helpviewer_keywords: ["ScriptGetLogicalWidths","ScriptGetLogicalWidths function [Internationalization for Windows Applications]","_win32_ScriptGetLogicalWidths","intl.scriptgetlogicalwidths","usp10/ScriptGetLogicalWidths"]
old-location: intl\scriptgetlogicalwidths.htm
tech.root: Intl
ms.assetid: ecedd0a1-aad8-4527-be46-6f7dd26a9e9b
ms.date: 12/05/2018
ms.keywords: ScriptGetLogicalWidths, ScriptGetLogicalWidths function [Internationalization for Windows Applications], _win32_ScriptGetLogicalWidths, intl.scriptgetlogicalwidths, usp10/ScriptGetLogicalWidths
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
 - ScriptGetLogicalWidths
 - usp10/ScriptGetLogicalWidths
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptGetLogicalWidths
---

# ScriptGetLogicalWidths function


## -description

Converts the glyph <a href="/windows/desktop/Intl/uniscribe-glossary">advance widths</a> for a specific font into logical widths.

## -parameters

### -param psa [in]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure.

### -param cChars [in]

Count of the logical code points in the run.

### -param cGlyphs [in]

Count of the glyphs in the run.

### -param piGlyphWidth [in]

Pointer to an array of glyph advance widths.

### -param pwLogClust [in]

Pointer to an array of logical clusters.

### -param psva [in]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a> structure defining visual attributes.

### -param piDx [out]

Pointer to an array of logical widths.

## -returns

Currently returns S_OK in all cases.

## -remarks

This function is useful for recording widths in a font-independent manner. It converts the glyph advance widths calculated for a specific font into logical widths, one per code point, in the same order as the code points. If the same string is then displayed on a different device using a different font, the logical widths can be applied by using <a href="/windows/desktop/api/usp10/nf-usp10-scriptapplylogicalwidth">ScriptApplyLogicalWidth</a> to approximate the original placement. This mechanism is useful when implementing print preview. On the preview screen, it is important to match the layout and placement of the final printed result.

<div class="alert"><b>Note</b>  Ligature glyph widths are divided evenly among the characters they represent.</div>
<div> </div>
<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptapplylogicalwidth">ScriptApplyLogicalWidth</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>