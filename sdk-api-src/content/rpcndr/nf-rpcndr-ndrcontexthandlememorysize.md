---
UID: NF:rpcndr.NdrContextHandleMemorySize
title: NdrContextHandleMemorySize function (rpcndr.h)
description: Returns the size of the supplied RPC context handle as represented in local memory.
helpviewer_keywords: ["NdrContextHandleMemorySize","NdrContextHandleMemorySize function [RPC]","rpc.ndrcontexthandlememorysize","rpcndr/NdrContextHandleMemorySize"]
old-location: rpc\ndrcontexthandlememorysize.htm
tech.root: Rpc
ms.assetid: f1dd8d13-8d10-4c5c-bb31-b51d38834e88
ms.date: 12/05/2018
ms.keywords: NdrContextHandleMemorySize, NdrContextHandleMemorySize function [RPC], rpc.ndrcontexthandlememorysize, rpcndr/NdrContextHandleMemorySize
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
 - NdrContextHandleMemorySize
 - rpcndr/NdrContextHandleMemorySize
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
 - NdrContextHandleMemorySize
---

# NdrContextHandleMemorySize function


## -description

The <b>NdrContextHandleMemorySize</b> function returns the size of the supplied RPC context handle as represented in local memory.

## -parameters

### -param pStubMsg

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that contains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the context handle, in bytes. Structure is for internal use only; do not modify.

### -param pFormat

Pointer to a <b>FORMAT_STRING</b> structure that contains the format of the context handle specified in <i>pMemory</i>.

## -returns

Returns the size of the context handle in memory, in bytes.

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-ndrcontexthandlesize">NdrContextHandleSize</a>