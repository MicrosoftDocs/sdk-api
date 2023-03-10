---
UID: NF:rpcndr.NdrClientCall2
title: NdrClientCall2 function (rpcndr.h)
description: The NdrClientCall2 function is the client-side entry point for the /Oicf mode stub.
helpviewer_keywords: ["NdrClientCall2","NdrClientCall2 function [RPC]","rpc.ndrclientcall2","rpcndr/NdrClientCall2"]
old-location: rpc\ndrclientcall2.htm
tech.root: Rpc
ms.assetid: 136b6461-048a-41ee-8514-0dea0861b2c1
ms.date: 12/05/2018
ms.keywords: NdrClientCall2, NdrClientCall2 function [RPC], rpc.ndrclientcall2, rpcndr/NdrClientCall2
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - NdrClientCall2
 - rpcndr/NdrClientCall2
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
 - NdrClientCall2
---

# NdrClientCall2 function


## -description

The <b>NdrClientCall2</b> function is the client-side entry point for the <a href="/windows/desktop/Midl/-oi">/Oicf</a> mode stub.

## -parameters

### -param pStubDescriptor [in]

Pointer to the MIDL-generated <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_desc">MIDL_STUB_DESC</a> structure that contains information about the description of the remote interface.

### -param pFormat [in]

Pointer to the MIDL-generated procedure format string that describes the method and parameters.

### -param ...

Pointer to the client-side calling stack.

## -returns

Return value of the remote call. The maximum size of a return value is equivalent to the register size of the system. MIDL switches to the <a href="/windows/desktop/Midl/-os">/Os</a> mode stub if the return value size is larger than the register size.

Depending on the method definition, this function can throw an exception if there is a network or server failure.

## -remarks

The <b>NdrClientCall2</b> function is used by all <a href="/windows/desktop/Midl/-oi">/Oicf</a> mode client-side stubs. The <b>NdrClientCall2</b> function transmits all [in] data to the remote server, and upon receipt of the response packet, returns the [out] value to the client-side application.

