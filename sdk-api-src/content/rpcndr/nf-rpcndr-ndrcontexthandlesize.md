---
UID: NF:rpcndr.NdrContextHandleSize
title: NdrContextHandleSize function
author: windows-sdk-content
description: The NdrContextHandleSize function returns the size of the supplied RPC context handle.
old-location: rpc\ndrcontexthandlesize.htm
old-project: Rpc
ms.assetid: f5f90887-67b2-4796-96b2-2607b9284387
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: NdrContextHandleSize, NdrContextHandleSize function [RPC], rpc.ndrcontexthandlesize, rpcndr/NdrContextHandleSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrContextHandleSize
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdrContextHandleSize function


## -description


The <b>NdrContextHandleSize</b> function returns the size of the supplied RPC context handle.


## -parameters




### -param pStubMsg

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that contains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the context handle, in bytes. Structure is for internal use only; do not modify.


### -param pMemory

Pointer to a string buffer that contains an RPC context handle.


### -param pFormat

Pointer to a <b>FORMAT_STRING</b> structure that contains the format of the context handle specified in <i>pMemory</i>.


## -returns



This function has no return value. However, it throws an exception upon error.




## -see-also




<a href="https://msdn.microsoft.com/f1dd8d13-8d10-4c5c-bb31-b51d38834e88">NdrContextHandleMemorySize</a>
 

 

