---
UID: NF:rpcndr.NdrStubCall2
title: NdrStubCall2 function (rpcndr.h)
description: The NdrStubCall2 function is the server-side entry point for /Oicf mode stubs.
helpviewer_keywords: ["NdrStubCall2","NdrStubCall2 function [RPC]","rpc.ndrstubcall2","rpcndr/NdrStubCall2"]
old-location: rpc\ndrstubcall2.htm
tech.root: Rpc
ms.assetid: 4249a73b-8e97-4e15-816e-a26a057d6a80
ms.date: 12/05/2018
ms.keywords: NdrStubCall2, NdrStubCall2 function [RPC], rpc.ndrstubcall2, rpcndr/NdrStubCall2
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
 - NdrStubCall2
 - rpcndr/NdrStubCall2
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
 - NdrStubCall2
---

# NdrStubCall2 function


## -description

The <b>NdrStubCall2</b> function is the server-side entry point for <a href="/windows/desktop/Midl/-oi">/Oicf</a> mode stubs.

## -parameters

### -param pThis [in]

Pointer to an instance of the CStdStubBuffer object, implementing  <a href="/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>, for the DCOM interface.  Set to <b>NULL</b> for nonobject RPC interfaces.

### -param pChannel [in]

Pointer to <a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a> for the DCOM interface, often provided by OLE. Set to <b>NULL</b> for nonobject interfaces.

### -param pRpcMsg [in, out]

Pointer to an <a href="/windows/desktop/api/rpcdcep/ns-rpcdcep-rpc_message">RPC_MESSAGE</a> structure that  contains information about the RPC request. In nonobject interfaces, <i>pRpcMsg</i> also contains information about the remoting method.

### -param pdwStubPhase [out]

Pointer to a flag that tracks the current interpreter call's activity.

## -returns

Returns S_OK upon success. Raises an exception upon error.

## -remarks

The RPC run-time or OLE run-time calls <b>NdrStubCall2</b> to invoke the server manager routine. The [out] parameters are marshalled and returned to RPC run-time or OLE run-time to send back to the client.

The <i>pdwStubPhase</i> parameter is used by the object interface to determine exception handling behavior. The following table describes possible values for the <i>pdwStubPhase</i> parameter.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>STUB_UNMARSHAL</td>
<td>The stub is in marshalling phase.</td>
</tr>
<tr>
<td>STUB_CALL_SERVER</td>
<td>The stub is calling a server manager routine.</td>
</tr>
<tr>
<td>STUB_MARSHAL</td>
<td>The stub is in unmarshalling phase.</td>
</tr>
<tr>
<td>STUB_CALL_SERVER_NO_HRESULT</td>
<td>Obsolete. For deprecated stubs only.</td>
</tr>
</table>