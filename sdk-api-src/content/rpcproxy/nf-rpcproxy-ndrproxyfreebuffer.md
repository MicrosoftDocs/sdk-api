---
UID: NF:rpcproxy.NdrProxyFreeBuffer
title: NdrProxyFreeBuffer function
author: windows-sdk-content
description: The NdrProxyFreeBuffer function frees an RPC buffer.
old-location: rpc\ndrproxyfreebuffer.htm
old-project: rpc
ms.assetid: 6abc3f93-6eef-4363-aa1a-1ecfffb9d934
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: NdrProxyFreeBuffer, NdrProxyFreeBuffer function [RPC], rpc.ndrproxyfreebuffer, rpcproxy/NdrProxyFreeBuffer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrProxyFreeBuffer
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrProxyFreeBuffer function


## -description


The <b>NdrProxyFreeBuffer</b> function frees an RPC buffer.


## -parameters




### -param This [in]

Pointer to the interface proxy.


### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>pRpcMsg</b> member points to a structure whose <b>Buffer</b> member is to be freed. Structure is for internal use only; do not modify.


## -returns



This function does not return a value.




## -remarks



The <b>NdrProxyFreeBuffer</b> function calls the <a href="_com_irpcchannelbuffer_freebuffer">IRpcChannelBuffer::FreeBuffer</a> method to free the RPC buffer and release <a href="_com_irpcchannelbuffer">IRpcChannelBuffer</a>.



