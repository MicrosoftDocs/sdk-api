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

# RPC_AUTH_KEY_RETRIEVAL_FN callback function


## -description


The 
<i>RPC_AUTH_KEY_RETRIEVAL_FN</i> function is a prototype for a function that specifies the address of a server-application-provided routine returning encryption keys.


## -parameters




### -param *Arg

Pointer to a user-defined argument to the user-supplied encryption key acquisition function. The RPC run-time library uses the <i>Arg</i> parameter supplied to 
<a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a>.


### -param ServerPrincName

Pointer to the principal name to use for the server when authenticating remote procedure calls. The RPC run-time library uses the <i>ServerPrincName</i> parameter supplied to 
<a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a>.


### -param KeyVer

Value that the RPC run-time library automatically provides for the key-version parameter. When the value is zero, the acquisition function must return the most recent key available.


#### - **Key

Pointer to a pointer to the authentication key returned by the user-supplied function.


### -param *Status

Pointer to the status returned by the acquisition function when it is called by the RPC run-time library to authenticate the client RPC request. If the status is other than RPC_S_OK, the request fails and the run-time library returns the error status to the client application.


#### - Key

Pointer to a pointer to the authentication key returned by the user-supplied function.


## -returns



This callback function does not return a value.




## -remarks



An authorization key–retrieval function specifies the address of a server-application-provided routine returning encryption keys.




## -see-also




<a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a>
 

 

