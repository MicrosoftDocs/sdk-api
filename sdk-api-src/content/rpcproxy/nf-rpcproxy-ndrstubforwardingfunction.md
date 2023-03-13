---
UID: NF:rpcproxy.NdrStubForwardingFunction
title: NdrStubForwardingFunction function (rpcproxy.h)
description: The NdrStubForwardingFunction function is the entry point for server-side object methods that are defined in a base interface.
helpviewer_keywords: ["NdrStubForwardingFunction","NdrStubForwardingFunction function [RPC]","rpc.ndrstubforwardingfunction","rpcproxy/NdrStubForwardingFunction"]
old-location: rpc\ndrstubforwardingfunction.htm
tech.root: Rpc
ms.assetid: 05d69090-4274-4dad-8fef-89db247d0c09
ms.date: 12/05/2018
ms.keywords: NdrStubForwardingFunction, NdrStubForwardingFunction function [RPC], rpc.ndrstubforwardingfunction, rpcproxy/NdrStubForwardingFunction
req.header: rpcproxy.h
req.include-header: 
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
 - NdrStubForwardingFunction
 - rpcproxy/NdrStubForwardingFunction
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
 - NdrStubForwardingFunction
---

# NdrStubForwardingFunction function


## -description

The <b>NdrStubForwardingFunction</b> function is the entry point for server-side object methods that are defined in a base interface.

## -parameters

### -param This [in]

Pointer to an instance of the CStdStubBuffer object, implementing <a href="/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>, for the DCOM interface.

### -param pChannel [in]

Pointer to <a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a> for the DCOM interface, often provided by OLE.

### -param pmsg [in, out]

Pointer to an <a href="/windows/desktop/api/rpcdcep/ns-rpcdcep-rpc_message">RPC_MESSAGE</a> structure that  contains information about the RPC request.

### -param pdwStubPhase [out]

Pointer to a flag that tracks the current interpreter call's activity.

## -remarks

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
 

For methods that are defined in a base interface, RPC needs to forward the code to the base interface implementation. 

For example: 


```cpp
Interface IFunctionSample: IUnknown

{

HRESULT FunctionSample();

}

Interface IOperation: IFunctionSample

{

HRESULT Operation();

}

```


In this example, where <b>IFunctionSample</b> and <b>IOperation</b> are defined in different .idl files. <b>IFunctionSample</b> is the base interface and <b>IOperation</b> is the derived interface. <b>IOperation</b> can aggregate <b>IOperation</b> without implementing <b>IOperation::FunctionSample</b>. When the client calls <b>IOperation::FunctionSample</b>, in the server side, RPC forwards the call to <b>IFunctionSample:FunctionSample</b>.