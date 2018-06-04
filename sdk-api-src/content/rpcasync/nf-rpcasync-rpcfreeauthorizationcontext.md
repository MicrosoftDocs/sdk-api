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

# RpcFreeAuthorizationContext function


## -description


The 
<b>RpcFreeAuthorizationContext</b> function frees an Authz context obtained by a previous call to the 
<a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a> function.


## -parameters




### -param pAuthzClientContext [in]

Pointer to the previously obtained Authz client context to be freed.


## -returns



Successful completion returns RPC_S_OK. This function does not fail unless an invalid parameter is provided.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The <i>pAuthzClientContext</i> parameter is a pointer to the Authz context, not the context itself. To prevent accidental reuse of the Authz context freed by this function call, RPC run-time zeros out the context upon return.




## -see-also




<a href="https://msdn.microsoft.com/a15c61f0-03cc-462f-b5c1-8e7f062e9523">Extended Error
		  Information</a>



<a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a>
 

 

