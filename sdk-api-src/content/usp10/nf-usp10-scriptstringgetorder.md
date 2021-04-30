---
UID: NF:usp10.ScriptStringGetOrder
title: ScriptStringGetOrder function (usp10.h)
description: Creates an array that maps an original character position to a glyph position.
helpviewer_keywords: ["ScriptStringGetOrder","ScriptStringGetOrder function [Internationalization for Windows Applications]","_win32_ScriptStringGetOrder","intl.scriptstringgetorder","usp10/ScriptStringGetOrder"]
old-location: intl\scriptstringgetorder.htm
tech.root: Intl
ms.assetid: c9986143-af15-439b-8c99-e07b48344645
ms.date: 12/05/2018
ms.keywords: ScriptStringGetOrder, ScriptStringGetOrder function [Internationalization for Windows Applications], _win32_ScriptStringGetOrder, intl.scriptstringgetorder, usp10/ScriptStringGetOrder
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
 - ScriptStringGetOrder
 - usp10/ScriptStringGetOrder
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
 - ScriptStringGetOrder
---

# ScriptStringGetOrder function


## -description

Creates an array that maps an original character position to a glyph position.

## -parameters

### -param ssa [in]

A <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure for the string.

### -param puOrder [out]

Pointer to a buffer in which this function retrieves an array of glyph positions, indexed by the original character position. The array should have room for at least the number of integers indicated by the <i>ssa</i> parameter of <a href="/windows/desktop/api/usp10/nf-usp10-scriptstring_pcoutchars">ScriptString_pcOutChars</a>.

## -returns

Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

When the number of glyphs and the number of characters are equal, the function retrieves an array that references every glyph. This is the same treatment that occurs in <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>.

To use this function, the application needs to specify SSA_GLYPHS in its original call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a>.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstring_pcoutchars">ScriptString_pcOutChars</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>