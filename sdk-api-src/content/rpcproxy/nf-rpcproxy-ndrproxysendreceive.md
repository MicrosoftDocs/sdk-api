---
UID: NF:rpcproxy.NdrProxySendReceive
title: NdrProxySendReceive function (rpcproxy.h)
description: The NdrProxySendReceive function sends a message to the server then waits for a reply.
helpviewer_keywords: ["NdrProxySendReceive","NdrProxySendReceive function [RPC]","rpc.ndrproxysendreceive","rpcproxy/NdrProxySendReceive"]
old-location: rpc\ndrproxysendreceive.htm
tech.root: Rpc
ms.assetid: a80c3271-bed3-4757-97e1-2bf212eaeafd
ms.date: 12/05/2018
ms.keywords: NdrProxySendReceive, NdrProxySendReceive function [RPC], rpc.ndrproxysendreceive, rpcproxy/NdrProxySendReceive
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
 - NdrProxySendReceive
 - rpcproxy/NdrProxySendReceive
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
 - NdrProxySendReceive
---

# NdrProxySendReceive function


## -description

The <b>NdrProxySendReceive</b> function sends a message to the server then waits for a reply.

## -parameters

### -param This [in]

Pointer to the interface proxy.

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.