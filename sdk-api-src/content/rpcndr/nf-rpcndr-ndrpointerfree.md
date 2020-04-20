---
UID: NF:rpcndr.NdrPointerFree
title: NdrPointerFree function (rpcndr.h)
description: The NdrPointerFree function frees memory.helpviewer_keywords: ["NdrPointerFree","NdrPointerFree function [RPC]","rpc.ndrpointerfree","rpcndr/NdrPointerFree"]
old-location: rpc\ndrpointerfree.htm
tech.root: Rpc
ms.assetid: 8b90ae12-af0f-41f8-9b8d-4b354de511be
ms.date: 12/05/2018
ms.keywords: NdrPointerFree, NdrPointerFree function [RPC], rpc.ndrpointerfree, rpcndr/NdrPointerFree
f1_keywords:
- rpcndr/NdrPointerFree
dev_langs:
- c++
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
- NdrPointerFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrPointerFree function


## -description


The <b>NdrPointerFree</b> function frees memory.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub.  This structure is for internal use only and should not be modified.


### -param pMemory [in]

Pointer to memory to be freed.


### -param pFormat [in]

Pointer to the format string description.


