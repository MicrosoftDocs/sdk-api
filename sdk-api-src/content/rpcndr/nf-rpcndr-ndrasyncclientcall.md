---
UID: NF:rpcndr.NdrAsyncClientCall
title: NdrAsyncClientCall function (rpcndr.h)
description: The NdrAsyncClientCall function is the asynchronous client-side entry point for the /Oi and /Oic mode stub.
helpviewer_keywords: ["NdrAsyncClientCall","NdrAsyncClientCall function [RPC]","rpc.ndrasyncclientcall","rpcndr/NdrAsyncClientCall"]
old-location: rpc\ndrasyncclientcall.htm
tech.root: Rpc
ms.assetid: 591f56de-6ceb-46d7-9720-cd2213605ef2
ms.date: 12/05/2018
ms.keywords: NdrAsyncClientCall, NdrAsyncClientCall function [RPC], rpc.ndrasyncclientcall, rpcndr/NdrAsyncClientCall
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NdrAsyncClientCall
 - rpcndr/NdrAsyncClientCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - NdrAsyncClientCall
---

# NdrAsyncClientCall function


## -description

The <b>NdrAsyncClientCall</b> function is the asynchronous client-side entry point for the <a href="/windows/desktop/Midl/-oi">/Oi</a> and <b>/Oic</b> mode stub.

## -parameters

### -param pStubDescriptor [in]

Pointer to the MIDL-generated <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_desc">MIDL_STUB_DESC</a> structure that contains information about the description of the remote interface.

### -param pFormat [in]

Pointer to the MIDL-generated procedure format string that describes the method and parameters.

### -param ...

Pointer to the client-side calling stack.

## -returns

Return value of the remote call. The maximum size of a return value is equivalent to the register size of the system. MIDL switches to the <a href="/windows/desktop/Midl/-os">/Os</a> mode stub if the return value size is larger than the register size.

Depending on the method definition, this function can throw an exception if there is a network or server failure.

