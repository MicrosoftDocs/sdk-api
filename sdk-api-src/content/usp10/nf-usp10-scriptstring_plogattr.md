---
UID: NF:usp10.ScriptString_pLogAttr
title: ScriptString_pLogAttr function (usp10.h)
description: Returns a pointer to a logical attributes buffer for an analyzed string.
helpviewer_keywords: ["ScriptString_pLogAttr","ScriptString_pLogAttr function [Internationalization for Windows Applications]","_win32_ScriptString_pLogAttr","intl.scriptstring_plogattr","usp10/ScriptString_pLogAttr"]
old-location: intl\scriptstring_plogattr.htm
tech.root: Intl
ms.assetid: ff898c79-2d37-4c0b-af83-2322ab7cf656
ms.date: 12/05/2018
ms.keywords: ScriptString_pLogAttr, ScriptString_pLogAttr function [Internationalization for Windows Applications], _win32_ScriptString_pLogAttr, intl.scriptstring_plogattr, usp10/ScriptString_pLogAttr
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
 - ScriptString_pLogAttr
 - usp10/ScriptString_pLogAttr
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
 - ScriptString_pLogAttr
---

# ScriptString_pLogAttr function


## -description

Returns a pointer to a logical attributes buffer for an analyzed string.

## -parameters

### -param ssa [in]

A <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure for the string.

## -returns

Returns a pointer to a buffer containing <a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a> structures defining logical attributes if successful. The function returns <b>NULL</b> if it does not succeed.

## -remarks

The pointer returned by this function is valid only until the application passes the associated <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure to <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringfree">ScriptStringFree</a>.

The logical attribute buffer contains at least the number of integers indicated by the <i>ssa</i> parameter of <a href="/windows/desktop/api/usp10/nf-usp10-scriptstring_pcoutchars">ScriptString_pcOutChars</a>.

When scanning the <a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a> array for a word break point, the application should look backward for the values of the <b>fWordStop</b> and <b>fWhiteSpace</b> members. <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a> just calls <a href="/windows/desktop/api/usp10/nf-usp10-scriptbreak">ScriptBreak</a> on each run, and <b>ScriptBreak</b> never sets <b>fWordBreak</b> on the first character of a run, because it has no information that the previous run ended in white space.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptbreak">ScriptBreak</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstringfree">ScriptStringFree</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstring_pcoutchars">ScriptString_pcOutChars</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>