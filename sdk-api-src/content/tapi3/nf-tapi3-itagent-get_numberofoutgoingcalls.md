---
UID: NF:tapi3.ITAgent.get_NumberOfOutgoingCalls
title: ITAgent::get_NumberOfOutgoingCalls
author: windows-sdk-content
description: The get_NumberOfOutgoingCalls method gets the number of outgoing non-ACD calls handled during by this agent.
old-location: tapi3\itagent_get_numberofoutgoingcalls.htm
old-project: Tapi
ms.assetid: fb2af58c-0b9e-4b00-8d8c-2fbfb2e0fc95
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITAgent interface [TAPI 2.2],get_NumberOfOutgoingCalls method, ITAgent.get_NumberOfOutgoingCalls, ITAgent::get_NumberOfOutgoingCalls, _tapi3_itagent_get_numberofoutgoingcalls, get_NumberOfOutgoingCalls, get_NumberOfOutgoingCalls method [TAPI 2.2], get_NumberOfOutgoingCalls method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_numberofoutgoingcalls, tapi3cc/ITAgent::get_NumberOfOutgoingCalls
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSP_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgent.get_NumberOfOutgoingCalls
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgent::get_NumberOfOutgoingCalls


## -description


The 
<b>get_NumberOfOutgoingCalls</b> method gets the number of outgoing non-ACD calls handled during by this agent.

The measurement period over which this information is calculated is switch- and/or implementation-specific. (See 
<a href="https://msdn.microsoft.com/ccc91dfb-83e5-496a-921d-784fcaea5af5">get_MeasurementPeriod</a>.)


## -parameters




### -param plCalls [out]

Total number of outgoing calls.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plCalls</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>
 

 

