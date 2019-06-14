---
UID: NF:rpcproxy.NdrProxySendReceive
title: NdrProxySendReceive function (rpcproxy.h)
author: windows-sdk-content
description: The NdrProxySendReceive function sends a message to the server then waits for a reply.
old-location: rpc\ndrproxysendreceive.htm
tech.root: Rpc
ms.assetid: a80c3271-bed3-4757-97e1-2bf212eaeafd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NdrProxySendReceive, NdrProxySendReceive function [RPC], rpc.ndrproxysendreceive, rpcproxy/NdrProxySendReceive
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
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrProxySendReceive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrProxySendReceive function


## -description


The <b>NdrProxySendReceive</b> function sends a message to the server then waits for a reply.


## -parameters




### -param This [in]

Pointer to the interface proxy.


### -param pStubMsg [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-_midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


## -returns



This function has no return values. Throws an exception upon error.



