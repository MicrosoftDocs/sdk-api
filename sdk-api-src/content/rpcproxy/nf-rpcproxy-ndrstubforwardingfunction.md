---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NdrStubForwardingFunction function


## -description


The <b>NdrStubForwardingFunction</b> function is the entry point for server-side object methods that are defined in a base interface.


## -parameters




### -param This

TBD


### -param pChannel [in]

Pointer to <a href="_com_irpcchannelbuffer">IRpcChannelBuffer</a> for the DCOM interface, often provided by OLE. 


### -param pmsg

TBD


### -param pdwStubPhase [out]

Pointer to a flag that tracks the current interpreter call's activity.


#### - pMsg [in, out]

Pointer to an <a href="https://msdn.microsoft.com/fd014622-97b3-4f76-8bc3-10821aa3c46e">RPC_MESSAGE</a> structure that  contains information about the RPC request.


#### - pThis [in]

Pointer to an instance of the CStdStubBuffer object, implementing <a href="_com_irpcstubbuffer">IRpcStubBuffer</a>, for the DCOM interface.  


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



