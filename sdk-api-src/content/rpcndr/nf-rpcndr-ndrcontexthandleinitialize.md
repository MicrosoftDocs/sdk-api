---
UID: NF:rpcndr.NdrContextHandleInitialize
title: NdrContextHandleInitialize function
author: windows-sdk-content
description: Initializes a new RPC context handle.
old-location: rpc\ndrcontexthandleinitialize.htm
tech.root: rpc
ms.assetid: 023f5137-fbdb-44c2-9c11-a3a8f1eb615e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NdrContextHandleInitialize, NdrContextHandleInitialize function [RPC], rpc.ndrcontexthandleinitialize, rpcndr/NdrContextHandleInitialize
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
 - NdrContextHandleInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrContextHandleInitialize function


## -description


The <b>NdrContextHandleInitialize</b> function initializes a new RPC context handle.


## -parameters




### -param pStubMsg

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that contains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param pFormat

Pointer to a <b>FORMAT_STRING</b> structure that contains the format of the new context handle.


## -returns



Returns a NDR_SCONTEXT structure that provides a newly initialized context on return or raises exception upon error.



