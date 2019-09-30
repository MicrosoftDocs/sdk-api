---
UID: NF:rpcproxy.NdrStubGetBuffer
title: NdrStubGetBuffer function (rpcproxy.h)
author: windows-sdk-content
description: The NdrStubGetBuffer function retrieves a buffer from the RPC channel.
old-location: rpc\ndrstubgetbuffer.htm
tech.root: Rpc
ms.assetid: ab877b5a-5c44-46eb-bd03-26410eccc765
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NdrStubGetBuffer, NdrStubGetBuffer function [RPC], rpc.ndrstubgetbuffer, rpcproxy/NdrStubGetBuffer
ms.topic: function
f1_keywords:
- rpcproxy/NdrStubGetBuffer
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
- NdrStubGetBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrStubGetBuffer function


## -description


The <b>NdrStubGetBuffer</b> function retrieves a buffer from the RPC channel.


## -parameters




### -param This [in]

Pointer to the stub.


### -param pRpcChannelBuffer [in]

Pointer to RPC channel.


### -param pStubMsg [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>pRpcMsg</b> member points to a structure whose <b>Buffer</b> member points to the newly allocated buffer. Structure is for internal use only; do not modify.


## -returns



This function has no return value. Throws an exception upon error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>
 

 

