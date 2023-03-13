---
UID: NF:rpcproxy.NdrProxyInitialize
title: NdrProxyInitialize function (rpcproxy.h)
description: The NdrProxyInitialize function initializes the proxy for an object method.
helpviewer_keywords: ["NdrProxyInitialize","NdrProxyInitialize function [RPC]","rpc.ndrproxyinitialize","rpcproxy/NdrProxyInitialize"]
old-location: rpc\ndrproxyinitialize.htm
tech.root: Rpc
ms.assetid: 54037337-9166-4023-8470-65ad247ceee5
ms.date: 12/05/2018
ms.keywords: NdrProxyInitialize, NdrProxyInitialize function [RPC], rpc.ndrproxyinitialize, rpcproxy/NdrProxyInitialize
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NdrProxyInitialize
 - rpcproxy/NdrProxyInitialize
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
 - NdrProxyInitialize
---

# NdrProxyInitialize function


## -description

The <b>NdrProxyInitialize</b> function initializes the proxy for an object method.

## -parameters

### -param This [in]

Pointer to the interface proxy.

### -param pRpcMsg [in]

Pointer to an <a href="/windows/desktop/api/rpcdcep/ns-rpcdcep-rpc_message">RPC_MESSAGE</a> structure that  contains information about the RPC request.

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.

### -param pStubDescriptor [in]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_desc">MIDL_STUB_DESC</a> structure that contains a descriptor for the RPC stub. Structure is for internal use only; do not modify.

### -param ProcNum [in]

Procedure  number for the object method.