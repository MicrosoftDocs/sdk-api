---
UID: NF:tapi3.ITAgent.get_NumberOfIncomingCalls
title: ITAgent::get_NumberOfIncomingCalls (tapi3.h)
description: The get_NumberOfIncomingCalls method (tapi3.h) gets the number of incoming non-ACD calls handled by this agent.
helpviewer_keywords: ["ITAgent interface [TAPI 2.2]","get_NumberOfIncomingCalls method","ITAgent.get_NumberOfIncomingCalls","ITAgent::get_NumberOfIncomingCalls","_tapi3_itagent_get_numberofincomingcalls","get_NumberOfIncomingCalls","get_NumberOfIncomingCalls method [TAPI 2.2]","get_NumberOfIncomingCalls method [TAPI 2.2]","ITAgent interface","tapi3.itagent_get_numberofincomingcalls","tapi3cc/ITAgent::get_NumberOfIncomingCalls"]
old-location: tapi3\itagent_get_numberofincomingcalls.htm
tech.root: tapi3
ms.assetid: d70073e9-a181-4f8d-b34f-95c8a24fe8d6
ms.date: 08/09/2022
ms.keywords: ITAgent interface [TAPI 2.2],get_NumberOfIncomingCalls method, ITAgent.get_NumberOfIncomingCalls, ITAgent::get_NumberOfIncomingCalls, _tapi3_itagent_get_numberofincomingcalls, get_NumberOfIncomingCalls, get_NumberOfIncomingCalls method [TAPI 2.2], get_NumberOfIncomingCalls method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_numberofincomingcalls, tapi3cc/ITAgent::get_NumberOfIncomingCalls
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAgent::get_NumberOfIncomingCalls
 - tapi3/ITAgent::get_NumberOfIncomingCalls
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgent.get_NumberOfIncomingCalls
---

# ITAgent::get_NumberOfIncomingCalls


## -description

The 
<b>get_NumberOfIncomingCalls</b> method gets the number of incoming non-ACD calls handled by this agent.

The measurement period over which this information is calculated is switch- and/or implementation-specific. (See 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-get_measurementperiod">get_MeasurementPeriod</a>.)

## -parameters

### -param plCalls [out]

Total number of incoming calls.

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

<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
