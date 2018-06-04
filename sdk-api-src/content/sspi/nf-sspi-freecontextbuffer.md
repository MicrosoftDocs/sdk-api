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

# FreeContextBuffer function


## -description



			The <b>FreeContextBuffer</b> function enables callers of <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> functions to free memory buffers allocated by the security package.


## -parameters




### -param pvContextBuffer [in]

A pointer to memory to be freed.


## -returns




						If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns a nonzero error code.




## -remarks



Memory buffers are typically allocated by the  <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> and <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> functions.

The <b>FreeContextBuffer</b> function can free any memory allocated by a security package.




## -see-also




<a href="authentication_functions.htm">SSPI Functions</a>
 

 

