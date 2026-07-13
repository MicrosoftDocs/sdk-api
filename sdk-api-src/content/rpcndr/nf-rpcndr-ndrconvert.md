---
UID: NF:rpcndr.NdrConvert
title: NdrConvert function (rpcndr.h)
description: The NdrConvert function converts the network buffer from the data representation of the sender to the data representation of the receiver if they are different.
helpviewer_keywords: ["NdrConvert","NdrConvert","NdrConvert function [RPC]","rpc.ndrconvert","rpcndr/NdrConvert"]
old-location: rpc\ndrconvert.htm
tech.root: Rpc
ms.assetid: ee9952c3-04e1-4fc0-a1fb-d50bc60e87f6
ms.date: 12/05/2018
ms.keywords: NdrConvert, NdrConvert, NdrConvert function [RPC], rpc.ndrconvert, rpcndr/NdrConvert
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
 - NdrConvert
 - rpcndr/NdrConvert
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
 - NdrConvert
---

# NdrConvert function


## -description

The <b>NdrConvert</b> function converts the network buffer from the data representation of the sender to the data representation of the receiver if they are different.

## -parameters

### -param pStubMsg [in]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>pRpcMsg</b> member points to a structure whose <b>Buffer</b> member contains the data to convert. This structure is for internal use only and should not be modified.

### -param pFormat [in]

Pointer to type format  of the data to convert.

## -returns

This function has no return values. If an error occurs, the function throws one of the following exception codes.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_BAD_STUB_DATA or RPC_X_INVALID_BOUND</td>
<td>The network  buffer is incorrect.</td>
</tr>
<tr>
<td>STATUS_ACCESS_VIOLATION</td>
<td>An access violation occurred.</td>
</tr>
<tr>
<td>RPC_S_INTERNAL_ERROR</td>
<td>An error occurred in RPC.</td>
</tr>
</table>

## -remarks

The <b>NdrConvert</b> function is used by all <a href="/windows/desktop/Midl/-oi">/Oi</a>, <b>/Oic</b>, and <a href="/windows/desktop/Midl/-os">/Os</a> mode  stubs.