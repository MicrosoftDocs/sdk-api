---
UID: NF:usp10.ScriptStringGetOrder
title: ScriptStringGetOrder function
author: windows-sdk-content
description: Creates an array that maps an original character position to a glyph position.
old-location: intl\scriptstringgetorder.htm
tech.root: Intl
ms.assetid: c9986143-af15-439b-8c99-e07b48344645
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ScriptStringGetOrder, ScriptStringGetOrder function [Internationalization for Windows Applications], _win32_ScriptStringGetOrder, intl.scriptstringgetorder, usp10/ScriptStringGetOrder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptStringGetOrder
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
---

# ScriptStringGetOrder function


## -description


Creates an array that maps an original character position to a glyph position.


## -parameters




### -param ssa [in]

A <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure for the string.


### -param puOrder [out]

Pointer to a buffer in which this function retrieves an array of glyph positions, indexed by the original character position. The array should have room for at least the number of integers indicated by the <i>ssa</i> parameter of <a href="https://msdn.microsoft.com/ad3f15cc-d4e9-4e71-a8c8-287bd62e9b15">ScriptString_pcOutChars</a>.


## -returns



Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



When the number of glyphs and the number of characters are equal, the function retrieves an array that references every glyph. This is the same treatment that occurs in <a href="https://msdn.microsoft.com/80d3f4b3-503b-4abb-826c-e5c09972ba2f">GetCharacterPlacement</a>.

To use this function, the application needs to specify SSA_GLYPHS in its original call to <a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a>.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a>



<a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a>



<a href="https://msdn.microsoft.com/ad3f15cc-d4e9-4e71-a8c8-287bd62e9b15">ScriptString_pcOutChars</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

