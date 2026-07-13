---
UID: NF:usp10.ScriptString_pSize
title: ScriptString_pSize function (usp10.h)
description: Returns a pointer to a SIZE structure for an analyzed string.
helpviewer_keywords: ["ScriptString_pSize","ScriptString_pSize function [Internationalization for Windows Applications]","_win32_ScriptString_pSize","intl.scriptstring_psize","usp10/ScriptString_pSize"]
old-location: intl\scriptstring_psize.htm
tech.root: Intl
ms.assetid: 2938e600-3f6b-4178-bc0f-bcbcd97b9d04
ms.date: 12/05/2018
ms.keywords: ScriptString_pSize, ScriptString_pSize function [Internationalization for Windows Applications], _win32_ScriptString_pSize, intl.scriptstring_psize, usp10/ScriptString_pSize
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
 - ScriptString_pSize
 - usp10/ScriptString_pSize
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
 - ScriptString_pSize
---

# ScriptString_pSize function


## -description

Returns a pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure for an analyzed string.

## -parameters

### -param ssa [in]

A <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure for a string.

## -returns

Returns a pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure containing the size (width and height) of the analyzed string if successful. The function returns <b>NULL</b> if it does not succeed.

## -remarks

The size returned by this function is the size before the effect of the justification requested by setting the SSA_FIT flag in <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a>. The difference between the value of <i>iReqWidth</i> in <b>ScriptStringAnalyse</b> and the size returned by <b>ScriptString_pSize</b> is the effect of justification.

The pointer returned by this function is valid only until the application passes the associated <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure to <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringfree">ScriptStringFree</a>.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstringfree">ScriptStringFree</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>