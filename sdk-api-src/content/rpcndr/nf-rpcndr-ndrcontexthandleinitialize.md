---
UID: NF:rpcndr.NdrContextHandleInitialize
title: NdrContextHandleInitialize function (rpcndr.h)
description: Initializes a new RPC context handle.
helpviewer_keywords: ["NdrContextHandleInitialize","NdrContextHandleInitialize function [RPC]","rpc.ndrcontexthandleinitialize","rpcndr/NdrContextHandleInitialize"]
old-location: rpc\ndrcontexthandleinitialize.htm
tech.root: Rpc
ms.assetid: 023f5137-fbdb-44c2-9c11-a3a8f1eb615e
ms.date: 12/05/2018
ms.keywords: NdrContextHandleInitialize, NdrContextHandleInitialize function [RPC], rpc.ndrcontexthandleinitialize, rpcndr/NdrContextHandleInitialize
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
 - NdrContextHandleInitialize
 - rpcndr/NdrContextHandleInitialize
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
 - NdrContextHandleInitialize
---

# NdrContextHandleInitialize function


## -description

The <b>NdrContextHandleInitialize</b> function initializes a new RPC context handle.

## -parameters

### -param pStubMsg

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that contains the current status of the RPC stub. Structure is for internal use only; do not modify.

### -param pFormat

Pointer to a <b>FORMAT_STRING</b> structure that contains the format of the new context handle.

## -returns

Returns a NDR_SCONTEXT structure that provides a newly initialized context on return or raises exception upon error.