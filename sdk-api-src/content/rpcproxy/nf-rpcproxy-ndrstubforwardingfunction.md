---
UID: NF:rpcproxy.NdrStubForwardingFunction
title: NdrStubForwardingFunction function
author: windows-sdk-content
description: The NdrStubForwardingFunction function is the entry point for server-side object methods that are defined in a base interface.
old-location: rpc\ndrstubforwardingfunction.htm
old-project: Rpc
ms.assetid: 05d69090-4274-4dad-8fef-89db247d0c09
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: NdrStubForwardingFunction, NdrStubForwardingFunction function [RPC], rpc.ndrstubforwardingfunction, rpcproxy/NdrStubForwardingFunction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcproxy.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrStubForwardingFunction
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrStubForwardingFunction function


## -description


The <b>NdrStubForwardingFunction</b> function is the entry point for server-side object methods that are defined in a base interface.


## -parameters




### -param This [in]

Pointer to an instance of the CStdStubBuffer object, implementing <a href="_com_irpcstubbuffer">IRpcStubBuffer</a>, for the DCOM interface.  


### -param pChannel [in]

Pointer to <a href="_com_irpcchannelbuffer">IRpcChannelBuffer</a> for the DCOM interface, often provided by OLE. 


### -param pmsg [in, out]

Pointer to an <a href="https://msdn.microsoft.com/fd014622-97b3-4f76-8bc3-10821aa3c46e">RPC_MESSAGE</a> structure that  contains information about the RPC request.


### -param pdwStubPhase [out]

Pointer to a flag that tracks the current interpreter call's activity.


## -returns



This function has no return value. Throws an exception upon error.




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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Interface IFunctionSample: IUnknown

{

HRESULT FunctionSample();

}

Interface IOperation: IFunctionSample

{

HRESULT Operation();

}
</pre>
</td>
</tr>
</table></span></div>
In this example, where <b>IFunctionSample</b> and <b>IOperation</b> are defined in different .idl files. <b>IFunctionSample</b> is the base interface and <b>IOperation</b> is the derived interface. <b>IOperation</b> can aggregate <b>IOperation</b> without implementing <b>IOperation::FunctionSample</b>. When the client calls <b>IOperation::FunctionSample</b>, in the server side, RPC forwards the call to <b>IFunctionSample:FunctionSample</b>.



