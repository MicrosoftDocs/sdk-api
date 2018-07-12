---
UID: NF:usp10.ScriptStringCPtoX
title: ScriptStringCPtoX function
author: windows-sdk-content
description: Retrieves the x coordinate for the leading or trailing edge of a character position.
old-location: intl\scriptstringcptox.htm
old-project: Intl
ms.assetid: 0cc16a26-0559-4e2a-a7ec-99a2a6ca2bcb
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ScriptStringCPtoX, ScriptStringCPtoX function [Internationalization for Windows Applications], _win32_ScriptStringCPtoX, intl.scriptstringcptox, usp10/ScriptStringCPtoX
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
 - ScriptStringCPtoX
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptStringCPtoX function


## -description


Retrieves the x coordinate for the leading or trailing edge of a character position.


## -parameters




### -param ssa [in]

A <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure for the string.


### -param icp [in]

Character position in the string.


### -param fTrailing [in]

<b>TRUE</b> to indicate the trailing edge of the character position (<i>icp</i>) that corresponds to the x coordinate. This parameter is set to <b>FALSE</b> to indicate the leading edge of the character position.


### -param pX [out]

Pointer to a buffer in which this function retrieves the x coordinate corresponding to the character position.


## -returns



Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

