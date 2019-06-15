---
UID: NF:rpcproxy.NdrStubInitialize
title: NdrStubInitialize function (rpcproxy.h)
author: windows-sdk-content
description: The NdrStubInitialize function is called by the server stub before unmarshalling. It sets up some stub message fields.
old-location: rpc\ndrstubinitialize.htm
tech.root: Rpc
ms.assetid: 078442d1-1e35-4679-b86d-0a9110977a7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NdrStubInitialize, NdrStubInitialize function [RPC], rpc.ndrstubinitialize, rpcproxy/NdrStubInitialize
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
 - NdrStubInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrStubInitialize function


## -description


The <b>NdrStubInitialize</b> function is called by the server stub before unmarshalling.
    It sets up some stub message fields.


## -parameters




### -param pRpcMsg [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/rpcdcep/ns-rpcdcep-_rpc_message">RPC_MESSAGE</a> structure which contains the RPC message.


### -param pStubMsg [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-_midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param pStubDescriptor [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-_midl_stub_desc">MIDL_STUB_DESC</a> structure that contains a descriptor for the RPC stub. Structure is for internal use only; do not modify.


### -param pRpcChannelBuffer [in]

Pointer to RPC channel buffer.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>
 

 

