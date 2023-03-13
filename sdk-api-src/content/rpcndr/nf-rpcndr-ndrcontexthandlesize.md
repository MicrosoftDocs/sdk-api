---
UID: NF:rpcndr.NdrContextHandleSize
title: NdrContextHandleSize function (rpcndr.h)
description: The NdrContextHandleSize function returns the size of the supplied RPC context handle.
helpviewer_keywords: ["NdrContextHandleSize","NdrContextHandleSize function [RPC]","rpc.ndrcontexthandlesize","rpcndr/NdrContextHandleSize"]
old-location: rpc\ndrcontexthandlesize.htm
tech.root: Rpc
ms.assetid: f5f90887-67b2-4796-96b2-2607b9284387
ms.date: 12/05/2018
ms.keywords: NdrContextHandleSize, NdrContextHandleSize function [RPC], rpc.ndrcontexthandlesize, rpcndr/NdrContextHandleSize
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - NdrContextHandleSize
 - rpcndr/NdrContextHandleSize
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
 - NdrContextHandleSize
---

# NdrContextHandleSize function


## -description

The <b>NdrContextHandleSize</b> function returns the size of the supplied RPC context handle.

## -parameters

### -param pStubMsg

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that contains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the context handle, in bytes. Structure is for internal use only; do not modify.

### -param pMemory

Pointer to a string buffer that contains an RPC context handle.

### -param pFormat

Pointer to a <b>FORMAT_STRING</b> structure that contains the format of the context handle specified in <i>pMemory</i>.

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-ndrcontexthandlememorysize">NdrContextHandleMemorySize</a>