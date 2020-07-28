---
UID: NF:tapi3cc.ITAgent.get_NumberOfOutgoingCalls
title: ITAgent::get_NumberOfOutgoingCalls (tapi3cc.h)
description: The get_NumberOfOutgoingCalls method gets the number of outgoing non-ACD calls handled during by this agent.
helpviewer_keywords: ["ITAgent interface [TAPI 2.2]","get_NumberOfOutgoingCalls method","ITAgent.get_NumberOfOutgoingCalls","ITAgent::get_NumberOfOutgoingCalls","_tapi3_itagent_get_numberofoutgoingcalls","get_NumberOfOutgoingCalls","get_NumberOfOutgoingCalls method [TAPI 2.2]","get_NumberOfOutgoingCalls method [TAPI 2.2]","ITAgent interface","tapi3.itagent_get_numberofoutgoingcalls","tapi3cc/ITAgent::get_NumberOfOutgoingCalls"]
old-location: tapi3\itagent_get_numberofoutgoingcalls.htm
tech.root: tapi3
ms.assetid: fb2af58c-0b9e-4b00-8d8c-2fbfb2e0fc95
ms.date: 12/05/2018
ms.keywords: ITAgent interface [TAPI 2.2],get_NumberOfOutgoingCalls method, ITAgent.get_NumberOfOutgoingCalls, ITAgent::get_NumberOfOutgoingCalls, _tapi3_itagent_get_numberofoutgoingcalls, get_NumberOfOutgoingCalls, get_NumberOfOutgoingCalls method [TAPI 2.2], get_NumberOfOutgoingCalls method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_numberofoutgoingcalls, tapi3cc/ITAgent::get_NumberOfOutgoingCalls
f1_keywords:
- tapi3cc/ITAgent.get_NumberOfOutgoingCalls
dev_langs:
- c++
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
- ITAgent.get_NumberOfOutgoingCalls
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAgent::get_NumberOfOutgoingCalls


## -description


The 
<b>get_NumberOfOutgoingCalls</b> method gets the number of outgoing non-ACD calls handled during by this agent.

The measurement period over which this information is calculated is switch- and/or implementation-specific. (See 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_measurementperiod">get_MeasurementPeriod</a>.)


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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
 

 

