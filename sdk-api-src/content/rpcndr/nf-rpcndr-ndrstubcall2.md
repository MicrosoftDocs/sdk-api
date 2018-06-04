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

# NdrStubCall2 function


## -description


The <b>NdrStubCall2</b> function is the server-side entry point for <a href="midl._oi">/Oicf</a> mode stubs.  


## -parameters




### -param pThis [in]

Pointer to an instance of the CStdStubBuffer object, implementing  <a href="_com_irpcstubbuffer">IRpcStubBuffer</a>, for the DCOM interface.  Set to <b>NULL</b> for nonobject RPC interfaces.


### -param pChannel [in]

Pointer to <a href="_com_irpcchannelbuffer">IRpcChannelBuffer</a> for the DCOM interface, often provided by OLE. Set to <b>NULL</b> for nonobject interfaces.


### -param pRpcMsg [in, out]

Pointer to an <a href="https://msdn.microsoft.com/fd014622-97b3-4f76-8bc3-10821aa3c46e">RPC_MESSAGE</a> structure that  contains information about the RPC request. In nonobject interfaces, <i>pRpcMsg</i> also contains information about the remoting method.


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
 



