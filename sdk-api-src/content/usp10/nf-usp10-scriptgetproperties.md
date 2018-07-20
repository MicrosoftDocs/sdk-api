---
UID: NF:usp10.ScriptGetProperties
title: ScriptGetProperties function
author: windows-sdk-content
description: Retrieves information about the current scripts.
old-location: intl\scriptgetproperties.htm
old-project: Intl
ms.assetid: 4799829d-8122-4bb4-839c-92f177cfd2da
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ScriptGetProperties, ScriptGetProperties function [Internationalization for Windows Applications], _win32_ScriptGetProperties, intl.scriptgetproperties, usp10/ScriptGetProperties
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
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptGetProperties
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptGetProperties function


## -description


Retrieves information about the current scripts.


## -parameters




### -param ppSp [out]

Pointer to an array of pointers to <a href="https://msdn.microsoft.com/473c1265-1c2c-48f3-a852-c701bebcf9eb">SCRIPT_PROPERTIES</a> structures indexed by script.


### -param piNumScripts [out]

Pointer to the number of scripts. The valid range for this value is 0 through <i>piNumScripts</i>-1.


## -returns



Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



See <a href="https://msdn.microsoft.com/75c5946b-de38-48d9-a5e2-1e0b2dc9f3c7">Determining If a Script Requires Glyph Shaping</a> for an example of the use of this function.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/473c1265-1c2c-48f3-a852-c701bebcf9eb">SCRIPT_PROPERTIES</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

