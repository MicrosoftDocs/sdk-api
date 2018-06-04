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

# RpcServerCompleteSecurityCallback function


## -description


The <b>RpcServerCompleteSecurityCallback</b> function completes an asynchronous security callback. This function can cause the call either to be dispatched or fail.


## -parameters




### -param BindingHandle [in]

The Server Call that this function dispatches or fails. 


### -param Status [in]

Specifies an RPC status. If this value is not <b>RPC_S_OK</b>, the Server Call is failed with a value of <b>RPC_S_ACCESS_DENIED</b>.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>

## -returns



This function returns RPCRTAPI RPC_STATUS.



