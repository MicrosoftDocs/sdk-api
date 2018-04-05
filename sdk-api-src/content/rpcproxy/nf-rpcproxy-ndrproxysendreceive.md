---
UID: NF:rpcproxy.NdrProxySendReceive
title: NdrProxySendReceive function
author: windows-driver-content
description: The NdrProxySendReceive function sends a message to the server then waits for a reply.
old-location: rpc\ndrproxysendreceive.htm
old-project: Rpc
ms.assetid: a80c3271-bed3-4757-97e1-2bf212eaeafd
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: NdrProxySendReceive, NdrProxySendReceive function [RPC], rpc.ndrproxysendreceive, rpcproxy/NdrProxySendReceive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcproxy.h
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
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RpcRT4.dll
api_name:
-	NdrProxySendReceive
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# NdrProxySendReceive function


## -description


The <b>NdrProxySendReceive</b> function sends a message to the server then waits for a reply.


## -parameters




### -param This [in]

Pointer to the interface proxy.


### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


## -returns



This function has no return values. Throws an exception upon error.



