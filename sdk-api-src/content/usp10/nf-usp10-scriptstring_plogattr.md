---
UID: NF:usp10.ScriptString_pLogAttr
title: ScriptString_pLogAttr function
author: windows-sdk-content
description: Returns a pointer to a logical attributes buffer for an analyzed string.
old-location: intl\scriptstring_plogattr.htm
tech.root: Intl
ms.assetid: ff898c79-2d37-4c0b-af83-2322ab7cf656
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ScriptString_pLogAttr, ScriptString_pLogAttr function [Internationalization for Windows Applications], _win32_ScriptString_pLogAttr, intl.scriptstring_plogattr, usp10/ScriptString_pLogAttr
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
 - Usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptString_pLogAttr
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
---

# ScriptString_pLogAttr function


## -description


Returns a pointer to a logical attributes buffer for an analyzed string.


## -parameters




### -param ssa [in]

A <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure for the string.


## -returns



Returns a pointer to a buffer containing <a href="https://msdn.microsoft.com/24131b04-870a-4841-b9cd-7a09497bd2e6">SCRIPT_LOGATTR</a> structures defining logical attributes if successful. The function returns <b>NULL</b> if it does not succeed.




## -remarks



The pointer returned by this function is valid only until the application passes the associated <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure to <a href="https://msdn.microsoft.com/39d633a7-def7-41ef-80e5-f4c5c90cebba">ScriptStringFree</a>.

The logical attribute buffer contains at least the number of integers indicated by the <i>ssa</i> parameter of <a href="https://msdn.microsoft.com/ad3f15cc-d4e9-4e71-a8c8-287bd62e9b15">ScriptString_pcOutChars</a>.

When scanning the <a href="https://msdn.microsoft.com/24131b04-870a-4841-b9cd-7a09497bd2e6">SCRIPT_LOGATTR</a> array for a word break point, the application should look backward for the values of the <b>fWordStop</b> and <b>fWhiteSpace</b> members. <a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a> just calls <a href="https://msdn.microsoft.com/1613819f-9473-4d9f-8a65-a109c9ef3f43">ScriptBreak</a> on each run, and <b>ScriptBreak</b> never sets <b>fWordBreak</b> on the first character of a run, because it has no information that the previous run ended in white space.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a>



<a href="https://msdn.microsoft.com/1613819f-9473-4d9f-8a65-a109c9ef3f43">ScriptBreak</a>



<a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a>



<a href="https://msdn.microsoft.com/39d633a7-def7-41ef-80e5-f4c5c90cebba">ScriptStringFree</a>



<a href="https://msdn.microsoft.com/ad3f15cc-d4e9-4e71-a8c8-287bd62e9b15">ScriptString_pcOutChars</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

