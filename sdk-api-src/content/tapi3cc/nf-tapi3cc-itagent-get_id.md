---
UID: NF:tapi3cc.ITAgent.get_ID
title: ITAgent::get_ID
author: windows-sdk-content
description: The get_ID method gets an agent's ID.
old-location: tapi3\itagent_get_id.htm
tech.root: TAPI
ms.assetid: e5045dd7-5a12-415e-b68a-f483f77f4887
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITAgent interface [TAPI 2.2],get_ID method, ITAgent.get_ID, ITAgent::get_ID, _tapi3_itagent_get_id, get_ID, get_ID method [TAPI 2.2], get_ID method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_id, tapi3cc/ITAgent::get_ID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3cc.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgent.get_ID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgent::get_ID


## -description


The 
<b>get_ID</b> method gets an agent's ID.


## -parameters




### -param ppID [out]

Pointer to <b>BSTR</b> containing agent ID.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_CALLCENTER_NO_AGENT_ID</b></dt>
</dl>
</td>
<td width="60%">
ITAgent was not created using 
<a href="https://msdn.microsoft.com/95c70e48-b990-47c7-a8b8-5fa3a84ec5ba">ITAgentHandler::CreateAgentWithID</a>, but with 
<a href="https://msdn.microsoft.com/f3242013-59a6-40f9-9bb1-0bc30f27311c">ITAgentHandler::CreateAgent</a>. No ID exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppID</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



This method is provided for interfacing with legacy switch solutions.

The application must free the memory allocated for the <i>ppID</i> parameter through 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when the variable is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>
 

 

