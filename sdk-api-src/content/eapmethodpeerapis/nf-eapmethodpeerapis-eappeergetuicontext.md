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

# EapPeerGetUIContext function


## -description


Obtains the user interface context from the EAP method. This function is always followed by the <a href="https://msdn.microsoft.com/16301c49-4415-4ebe-abdd-a03183db5f20">EapPeerInvokeInteractiveUI</a> function, which is followed by the <a href="https://msdn.microsoft.com/90a3844b-5fe9-44ad-981a-0aae643b2390">EapPeerSetUIContext</a> function.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.


### -param pdwSizeOfUIContextData [out]

A pointer to a value that specifies the size of the user interface context data byte buffer returned in <i>ppUIContextData</i>.


### -param ppUIContextData [out]

A pointer to an address that contains a byte buffer with the supplicant user interface context data from EAPHost.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



<b>EapPeerGetUIContext</b> is called by EAPHost when a prior call indicates that a user interface context is available.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>



<a href="https://msdn.microsoft.com/16301c49-4415-4ebe-abdd-a03183db5f20">EapPeerInvokeInteractiveUI</a>



<a href="https://msdn.microsoft.com/90a3844b-5fe9-44ad-981a-0aae643b2390">EapPeerSetUIContext</a>
 

 

