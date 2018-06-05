---
UID: NF:rpcdce.RpcServerCompleteSecurityCallback
title: RpcServerCompleteSecurityCallback function
author: windows-sdk-content
description: The RpcServerCompleteSecurityCallback function completes an asynchronous security callback.
old-location: rpc\rpcservercompletesecuritycallback.htm
old-project: Rpc
ms.assetid: 4DF613C7-CF82-47DB-9D6A-F820373534E6
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: RpcServerCompleteSecurityCallback, RpcServerCompleteSecurityCallback function [RPC], rpc.rpcservercompletesecuritycallback, rpcdce/RpcServerCompleteSecurityCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcServerCompleteSecurityCallback
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



