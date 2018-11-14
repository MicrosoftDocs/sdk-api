---
UID: NF:rpcndr.NdrContextHandleMemorySize
title: NdrContextHandleMemorySize function
author: windows-sdk-content
description: Returns the size of the supplied RPC context handle as represented in local memory.
old-location: rpc\ndrcontexthandlememorysize.htm
tech.root: rpc
ms.assetid: f1dd8d13-8d10-4c5c-bb31-b51d38834e88
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: NdrContextHandleMemorySize, NdrContextHandleMemorySize function [RPC], rpc.ndrcontexthandlememorysize, rpcndr/NdrContextHandleMemorySize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - NdrContextHandleMemorySize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NdrContextHandleMemorySize
: 
---

# NdrContextHandleMemorySize function


## -description


The <b>NdrContextHandleMemorySize</b> function returns the size of the supplied RPC context handle as represented in local memory.


## -parameters




### -param pStubMsg

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that contains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the context handle, in bytes. Structure is for internal use only; do not modify.


### -param pFormat

Pointer to a <b>FORMAT_STRING</b> structure that contains the format of the context handle specified in <i>pMemory</i>.


## -returns



Returns the size of the context handle in memory, in bytes.




## -see-also




<a href="https://msdn.microsoft.com/f5f90887-67b2-4796-96b2-2607b9284387">NdrContextHandleSize</a>
 

 

