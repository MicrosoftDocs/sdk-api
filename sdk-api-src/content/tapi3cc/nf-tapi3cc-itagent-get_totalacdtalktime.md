---
UID: NF:tapi3cc.ITAgent.get_TotalACDTalkTime
title: ITAgent::get_TotalACDTalkTime (tapi3cc.h)
description: The ITAgent::get_TotalACDTalkTime method (tapi3cc.h) gets the number of seconds spent talking in ACD calls by this agent, across all sessions.
helpviewer_keywords: ["ITAgent interface [TAPI 2.2]","get_TotalACDTalkTime method","ITAgent.get_TotalACDTalkTime","ITAgent::get_TotalACDTalkTime","_tapi3_itagent_get_totalacdtalktime","get_TotalACDTalkTime","get_TotalACDTalkTime method [TAPI 2.2]","get_TotalACDTalkTime method [TAPI 2.2]","ITAgent interface","tapi3.itagent_get_totalacdtalktime","tapi3cc/ITAgent::get_TotalACDTalkTime"]
old-location: tapi3\itagent_get_totalacdtalktime.htm
tech.root: tapi3
ms.assetid: a622a812-c929-413a-a3bc-4e870158cf16
ms.date: 08/10/2022
ms.keywords: ITAgent interface [TAPI 2.2],get_TotalACDTalkTime method, ITAgent.get_TotalACDTalkTime, ITAgent::get_TotalACDTalkTime, _tapi3_itagent_get_totalacdtalktime, get_TotalACDTalkTime, get_TotalACDTalkTime method [TAPI 2.2], get_TotalACDTalkTime method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_totalacdtalktime, tapi3cc/ITAgent::get_TotalACDTalkTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAgent::get_TotalACDTalkTime
 - tapi3cc/ITAgent::get_TotalACDTalkTime
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
 - ITAgent.get_TotalACDTalkTime
---

# ITAgent::get_TotalACDTalkTime


## -description

The 
<b>get_TotalACDTalkTime</b> gets the number of seconds spent talking in ACD calls by this agent (across all sessions).

The measurement period over which this information is calculated is switch- and/or implementation-specific. (See 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-get_measurementperiod">get_MeasurementPeriod</a>.)

## -parameters

### -param plTalkTime [out]

Total talk time.

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
The <i>plTalkTime</i> parameter is not a valid pointer.

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
