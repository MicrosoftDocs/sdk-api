---
UID: NF:usp10.ScriptString_pcOutChars
title: ScriptString_pcOutChars function (usp10.h)
description: Returns a pointer to the length of a string after clipping.
helpviewer_keywords: ["ScriptString_pcOutChars","ScriptString_pcOutChars function [Internationalization for Windows Applications]","_win32_ScriptString_pcOutChars","intl.scriptstring_pcoutchars","usp10/ScriptString_pcOutChars"]
old-location: intl\scriptstring_pcoutchars.htm
tech.root: Intl
ms.assetid: ad3f15cc-d4e9-4e71-a8c8-287bd62e9b15
ms.date: 12/05/2018
ms.keywords: ScriptString_pcOutChars, ScriptString_pcOutChars function [Internationalization for Windows Applications], _win32_ScriptString_pcOutChars, intl.scriptstring_pcoutchars, usp10/ScriptString_pcOutChars
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
 - ScriptString_pcOutChars
 - usp10/ScriptString_pcOutChars
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
 - ScriptString_pcOutChars
---

# ScriptString_pcOutChars function


## -description

Returns a pointer to the length of a string after clipping.

## -parameters

### -param ssa [in]

A <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure for the string.

## -returns

Returns a pointer to the length of the string after clipping if successful. The length is the number of Unicode code points. The function returns <b>NULL</b> if it does not succeed.

## -remarks

To use this function, the application needs to specify SSA_CLIP in its original call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a>.

The pointer returned by this function is valid only until the application passes the associated <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure to <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringfree">ScriptStringFree</a>.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstringfree">ScriptStringFree</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>