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

# ImmDestroyContext function


## -description


Releases the input context and frees associated memory.


## -parameters




### -param HIMC

TBD




#### - hIMC [in]

Handle to the input context to free.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



Any application that creates an input context by using the <a href="https://msdn.microsoft.com/2207927a-0edb-4d3a-a1b7-75b94d1616d5">ImmCreateContext</a> function must call this function to free the context before it terminates. However, before calling <b>ImmDestroyContext</b>, the application must remove the input context from any association with windows in the thread by using the <a href="https://msdn.microsoft.com/978ea304-c44d-4f00-b86f-932bbd5f603c">ImmAssociateContext</a> function.




## -see-also




<a href="https://msdn.microsoft.com/978ea304-c44d-4f00-b86f-932bbd5f603c">ImmAssociateContext</a>



<a href="https://msdn.microsoft.com/2207927a-0edb-4d3a-a1b7-75b94d1616d5">ImmCreateContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

