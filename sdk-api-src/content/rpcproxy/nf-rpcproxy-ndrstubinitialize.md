---
UID: NF:rpcproxy.NdrStubInitialize
title: NdrStubInitialize function
author: windows-sdk-content
description: The NdrStubInitialize function is called by the server stub before unmarshalling. It sets up some stub message fields.
old-location: rpc\ndrstubinitialize.htm
tech.root: Rpc
ms.assetid: 078442d1-1e35-4679-b86d-0a9110977a7c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NdrStubInitialize, NdrStubInitialize function [RPC], rpc.ndrstubinitialize, rpcproxy/NdrStubInitialize
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
 - NdrStubInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrStubInitialize function


## -description


The <b>NdrStubInitialize</b> function is called by the server stub before unmarshalling.
    It sets up some stub message fields.


## -parameters




### -param pRpcMsg [in]

Pointer to the <a href="https://msdn.microsoft.com/fd014622-97b3-4f76-8bc3-10821aa3c46e">RPC_MESSAGE</a> structure which contains the RPC message.


### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param pStubDescriptor [in]

Pointer to a <a href="https://msdn.microsoft.com/e3178aaa-a30a-43ba-a78a-a28d6f20fa74">MIDL_STUB_DESC</a> structure that contains a descriptor for the RPC stub. Structure is for internal use only; do not modify.


### -param pRpcChannelBuffer [in]

Pointer to RPC channel buffer.


## -returns



This function does not return a value.




## -see-also




<a href="_com_irpcchannelbuffer">IRpcChannelBuffer</a>
 

 

