---
UID: NF:rpcproxy.NdrStubGetBuffer
title: NdrStubGetBuffer function
author: windows-sdk-content
description: The NdrStubGetBuffer function retrieves a buffer from the RPC channel.
old-location: rpc\ndrstubgetbuffer.htm
tech.root: rpc
ms.assetid: ab877b5a-5c44-46eb-bd03-26410eccc765
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: NdrStubGetBuffer, NdrStubGetBuffer function [RPC], rpc.ndrstubgetbuffer, rpcproxy/NdrStubGetBuffer
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NdrStubGetBuffer
: 
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

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>pRpcMsg</b> member points to a structure whose <b>Buffer</b> member points to the newly allocated buffer. Structure is for internal use only; do not modify.


## -returns



This function has no return value. Throws an exception upon error.




## -see-also




<a href="_com_irpcchannelbuffer">IRpcChannelBuffer</a>



<a href="_com_irpcstubbuffer">IRpcStubBuffer</a>
 

 

