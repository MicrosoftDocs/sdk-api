---
UID: NF:rpcproxy.NdrProxyGetBuffer
title: NdrProxyGetBuffer function (rpcproxy.h)
description: The NdrProxyGetBuffer function obtains a network buffer from COM through the use of an IRpcChannelBuffer::GetBuffer method call.
helpviewer_keywords: ["NdrProxyGetBuffer","NdrProxyGetBuffer function [RPC]","rpc.ndrproxygetbuffer","rpcproxy/NdrProxyGetBuffer"]
old-location: rpc\ndrproxygetbuffer.htm
tech.root: Rpc
ms.assetid: cdc07d50-a6cf-4107-9676-f48156fed1ca
ms.date: 12/05/2018
ms.keywords: NdrProxyGetBuffer, NdrProxyGetBuffer function [RPC], rpc.ndrproxygetbuffer, rpcproxy/NdrProxyGetBuffer
f1_keywords:
- rpcproxy/NdrProxyGetBuffer
dev_langs:
- c++
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
- NdrProxyGetBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrProxyGetBuffer function


## -description


The <b>NdrProxyGetBuffer</b> function obtains a network buffer from COM through the use of an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-getbuffer">IRpcChannelBuffer::GetBuffer</a> method call.


## -parameters




### -param This [in]

Pointer to the interface proxy.


### -param pStubMsg [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>pRpcMsg</b> member points to a structure whose <b>Buffer</b> member points to the newly allocated buffer. Structure is for internal use only; do not modify.


