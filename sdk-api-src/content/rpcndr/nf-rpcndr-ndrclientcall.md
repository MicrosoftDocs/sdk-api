---
UID: NF:rpcndr.NdrClientCall
title: NdrClientCall function (rpcndr.h)
description: The NdrClientCall function is the client-side entry point for the /Oicf mode stub.
helpviewer_keywords: ["NdrClientCall","NdrClientCall function [RPC]","rpc.ndrclientcall","rpcndr/NdrClientCall"]
old-location: rpc\ndrclientcall.htm
tech.root: Rpc
ms.assetid: c7bf480a-a9c7-4d67-a7b6-cba6352b4600
ms.date: 12/05/2018
ms.keywords: NdrClientCall, NdrClientCall function [RPC], rpc.ndrclientcall, rpcndr/NdrClientCall
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
 - NdrClientCall
 - rpcndr/NdrClientCall
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
 - NdrClientCall
---

# NdrClientCall function


## -description

The <b>NdrClientCall</b> function is the client-side entry point for the <a href="/windows/desktop/Midl/-oi">/Oicf</a> mode stub.

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

The <b>NdrClientCall</b> function is used by the <a href="/windows/desktop/Midl/-oi">/Oicf /robust</a>  client-side stub. The <b>/Oi</b> and <b>/Oic</b> client-side stubs are obsolete as of MIDL version 6.0.359 and should not be used. The <b>NdrClientCall</b> function transmits all [in] data to the remote server, and upon receipt of the response packet, returns the [out] value to the client-side application.

## -see-also

<a href="/windows/desktop/Midl/-oi">/Oicf</a>



<a href="/windows/desktop/Midl/-robust">/robust</a>

