---
UID: NF:tapi3.ITAgentSession.get_ACDGroup
title: ITAgentSession::get_ACDGroup
author: windows-sdk-content
description: The get_ACDGroup method gets the ACD group associated with this session.
old-location: tapi3\itagentsession_get_acdgroup.htm
tech.root: tapi
ms.assetid: ec80092d-ceff-432c-ba0a-695718b890af
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAgentSession interface [TAPI 2.2],get_ACDGroup method, ITAgentSession.get_ACDGroup, ITAgentSession::get_ACDGroup, _tapi3_itagentsession_get_acdgroup, get_ACDGroup, get_ACDGroup method [TAPI 2.2], get_ACDGroup method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_acdgroup, tapi3cc/ITAgentSession::get_ACDGroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3.h
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
 - ITAgentSession.get_ACDGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3.h
: 
- ITAgentSession.get_ACDGroup
: 
---

# ITAgentSession::get_ACDGroup


## -description


The 
<b>get_ACDGroup</b> method gets the ACD group associated with this session.


## -parameters




### -param ppACDGroup [out]

Pointer to 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppACDGroup</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LINEERR_</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="https://msdn.microsoft.com/06a5ea23-4205-46fd-abe7-ee4575be81c8">lineGetAgentSessionInfo</a> for error codes returned from this TAPI 2.1 function.

</td>
</tr>
</table>
 




## -remarks



This method wraps the TAPI 2.1 
<a href="https://msdn.microsoft.com/06a5ea23-4205-46fd-abe7-ee4575be81c8">lineGetAgentSessionInfo</a> function.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface returned by <b>ITAgentSession::get_ACDGroup</b>. The application must call <b>Release</b> on the 
<b>ITACDGroup</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>



<a href="https://msdn.microsoft.com/06a5ea23-4205-46fd-abe7-ee4575be81c8">lineGetAgentSessionInfo</a>
 

 

