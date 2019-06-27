---
UID: NF:rpcproxy.NdrProxyFreeBuffer
title: NdrProxyFreeBuffer function (rpcproxy.h)
author: windows-sdk-content
description: The NdrProxyFreeBuffer function frees an RPC buffer.
old-location: rpc\ndrproxyfreebuffer.htm
tech.root: Rpc
ms.assetid: 6abc3f93-6eef-4363-aa1a-1ecfffb9d934
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NdrProxyFreeBuffer, NdrProxyFreeBuffer function [RPC], rpc.ndrproxyfreebuffer, rpcproxy/NdrProxyFreeBuffer
ms.topic: function
f1_keywords: 
 - "rpcproxy/NdrProxyFreeBuffer"
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
 - NdrProxyFreeBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrProxyFreeBuffer function


## -description


The <b>NdrProxyFreeBuffer</b> function frees an RPC buffer.


## -parameters




### -param This [in]

Pointer to the interface proxy.


### -param pStubMsg [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-_midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>pRpcMsg</b> member points to a structure whose <b>Buffer</b> member is to be freed. Structure is for internal use only; do not modify.


## -returns



This function does not return a value.




## -remarks



The <b>NdrProxyFreeBuffer</b> function calls the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-freebuffer">IRpcChannelBuffer::FreeBuffer</a> method to free the RPC buffer and release <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>.



