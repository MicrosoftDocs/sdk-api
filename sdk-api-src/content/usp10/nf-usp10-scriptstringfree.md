---
UID: NF:usp10.ScriptStringFree
title: ScriptStringFree function (usp10.h)
description: Frees a SCRIPT_STRING_ANALYSIS structure.
old-location: intl\scriptstringfree.htm
tech.root: Intl
ms.assetid: 39d633a7-def7-41ef-80e5-f4c5c90cebba
ms.date: 12/05/2018
ms.keywords: ScriptStringFree, ScriptStringFree function [Internationalization for Windows Applications], _win32_ScriptStringFree, intl.scriptstringfree, usp10/ScriptStringFree
f1_keywords:
- usp10/ScriptStringFree
dev_langs:
- c++
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
- ScriptStringFree
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
---

# ScriptStringFree function


## -description


Frees a <a href="https://docs.microsoft.com/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure.


## -parameters




### -param pssa [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure.


## -returns



Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



When your application is finished with a <a href="https://docs.microsoft.com/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure, it should free the associated memory by calling this function. After this function is called, the pointers retrieved from <a href="https://docs.microsoft.com/windows/desktop/api/usp10/nf-usp10-scriptstring_pcoutchars">ScriptString_pcOutChars</a>, <a href="https://docs.microsoft.com/windows/desktop/api/usp10/nf-usp10-scriptstring_plogattr">ScriptString_pLogAttr</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/usp10/nf-usp10-scriptstring_psize">ScriptString_pSize</a> that are associated with the <i>pssa</i> parameter are invalid.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/usp10/nf-usp10-scriptstring_plogattr">ScriptString_pLogAttr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/usp10/nf-usp10-scriptstring_psize">ScriptString_pSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/usp10/nf-usp10-scriptstring_pcoutchars">ScriptString_pcOutChars</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>
 

 

