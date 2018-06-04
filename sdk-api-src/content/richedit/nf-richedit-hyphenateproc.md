---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# HyphenateProc function


## -description


The <i>HyphenateProc</i> function is an application–defined
		callback function used with the <a href="https://msdn.microsoft.com/67126cb8-ab50-49a9-b32f-2245debf2fe3">EM_SETHYPHENATEINFO</a> message. It determines how hyphenation is done in a Microsoft Rich Edit control.


## -parameters




### -param pszWord [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WCHAR</a>*</b>

Pointer to the word to hyphenate. 


### -param langid [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LANGID</a></b>

Current language ID for the control. 


### -param ichExceed [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Index of the character in the passed string that exceeds the line width.


### -param phyphresult [out]

Type: <b><a href="https://msdn.microsoft.com/43b9d78f-5931-49bd-8c58-cc333a3f3756">HYPHRESULT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/43b9d78f-5931-49bd-8c58-cc333a3f3756">HYPHRESULT</a> structure that <i>HyphenateProc</i> fills in with the result of the hyphenation. 


## -returns



There is no return value.




## -remarks



<i>HyphenateProc</i> is a placeholder for the application-defined function name.

An application must install the callback function by specifying the address of the callback function in an <a href="https://msdn.microsoft.com/67126cb8-ab50-49a9-b32f-2245debf2fe3">EM_SETHYPHENATEINFO</a> message. 




## -see-also




<a href="https://msdn.microsoft.com/67126cb8-ab50-49a9-b32f-2245debf2fe3">EM_SETHYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/2463189e-98cf-4545-a435-474df74e1a22">HYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/43b9d78f-5931-49bd-8c58-cc333a3f3756">HYPHRESULT</a>



<b>Reference</b>
 

 

