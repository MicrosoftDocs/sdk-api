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

# RPC_IF_CALLBACK_FN callback function


## -description


The 
<b>RPC_IF_CALLBACK_FN</b> is a prototype for a security-callback function that your application supplies. Your program can provide a callback function for each interface it defines.


## -parameters




### -param InterfaceUuid


### -param *Context [in]

Pointer to an RPC_IF_ID server binding handle representing the client. In the function declaration, this must be of type RPC_IF_HANDLE, but it is a client binding handle and can be safely cast to it. The callback function may pass this handle to 
<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a>, 
<a href="https://msdn.microsoft.com/9fdcdb99-be6c-4a3b-97dd-8d0eadd2754d">RpcBindingServerFromClient</a>,  <a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a>, or any other server side function that accepts a client binding handle to obtain information about the client.


#### - Interface [in]

UUID and version of the interface.


## -returns



The callback function should return RPC_S_OK if the client is allowed to call methods in this interface. Any other return code will cause the client to receive the exception RPC_S_ACCESS_DENIED.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



In some cases, the RPC run time may call the security-callback function more than once per client per interface. Be sure your callback function can handle this possibility.

The security callback must be declared as RPC_ENTRY.




## -see-also




<a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a>
 

 

