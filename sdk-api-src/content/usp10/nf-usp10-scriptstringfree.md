---
UID: NF:usp10.ScriptStringFree
title: ScriptStringFree function
author: windows-driver-content
description: Frees a SCRIPT_STRING_ANALYSIS structure.
old-location: intl\scriptstringfree.htm
old-project: Intl
ms.assetid: 39d633a7-def7-41ef-80e5-f4c5c90cebba
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: ScriptStringFree, ScriptStringFree function [Internationalization for Windows Applications], _win32_ScriptStringFree, intl.scriptstringfree, usp10/ScriptStringFree
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
req.typenames: SCRIPT_JUSTIFY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Usp10.dll
-	Ext-MS-Win-usp10-l1-1-0.dll
-	GDI32.dll
-	GDI32Full.dll
api_name:
-	ScriptStringFree
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptStringFree function


## -description


Frees a <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure.


## -parameters




### -param pssa [in, out]

Pointer to a <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure.


## -returns



Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



When your application is finished with a <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure, it should free the associated memory by calling this function. After this function is called, the pointers retrieved from <a href="https://msdn.microsoft.com/ad3f15cc-d4e9-4e71-a8c8-287bd62e9b15">ScriptString_pcOutChars</a>, <a href="https://msdn.microsoft.com/ff898c79-2d37-4c0b-af83-2322ab7cf656">ScriptString_pLogAttr</a>, and <a href="https://msdn.microsoft.com/2938e600-3f6b-4178-bc0f-bcbcd97b9d04">ScriptString_pSize</a> that are associated with the <i>pssa</i> parameter are invalid.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a>



<a href="https://msdn.microsoft.com/ff898c79-2d37-4c0b-af83-2322ab7cf656">ScriptString_pLogAttr</a>



<a href="https://msdn.microsoft.com/2938e600-3f6b-4178-bc0f-bcbcd97b9d04">ScriptString_pSize</a>



<a href="https://msdn.microsoft.com/ad3f15cc-d4e9-4e71-a8c8-287bd62e9b15">ScriptString_pcOutChars</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

