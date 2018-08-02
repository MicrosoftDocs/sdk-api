---
UID: NF:usp10.ScriptString_pSize
title: ScriptString_pSize function
author: windows-sdk-content
description: Returns a pointer to a SIZE structure for an analyzed string.
old-location: intl\scriptstring_psize.htm
old-project: Intl
ms.assetid: 2938e600-3f6b-4178-bc0f-bcbcd97b9d04
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ScriptString_pSize, ScriptString_pSize function [Internationalization for Windows Applications], _win32_ScriptString_pSize, intl.scriptstring_psize, usp10/ScriptString_pSize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SCRIPT_JUSTIFY
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
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptString_pSize function


## -description


Returns a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure for an analyzed string.


## -parameters




### -param ssa [in]

A <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure for a string.


## -returns



Returns a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure containing the size (width and height) of the analyzed string if successful. The function returns <b>NULL</b> if it does not succeed.




## -remarks



The size returned by this function is the size before the effect of the justification requested by setting the SSA_FIT flag in <a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a>. The difference between the value of <i>iReqWidth</i> in <b>ScriptStringAnalyse</b> and the size returned by <b>ScriptString_pSize</b> is the effect of justification.

The pointer returned by this function is valid only until the application passes the associated <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure to <a href="https://msdn.microsoft.com/39d633a7-def7-41ef-80e5-f4c5c90cebba">ScriptStringFree</a>.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a>



<a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a>



<a href="https://msdn.microsoft.com/39d633a7-def7-41ef-80e5-f4c5c90cebba">ScriptStringFree</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

