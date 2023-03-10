---
UID: NF:tapi3cc.ITAgent.get_TotalACDCallTime
title: ITAgent::get_TotalACDCallTime (tapi3cc.h)
description: The ITAgent::get_TotalACDCallTime method (tapi3cc.h) gets the number of seconds spent on ACD calls by this agent, across all sessions. 
helpviewer_keywords: ["ITAgent interface [TAPI 2.2]","get_TotalACDCallTime method","ITAgent.get_TotalACDCallTime","ITAgent::get_TotalACDCallTime","_tapi3_itagent_get_totalacdcalltime","get_TotalACDCallTime","get_TotalACDCallTime method [TAPI 2.2]","get_TotalACDCallTime method [TAPI 2.2]","ITAgent interface","tapi3.itagent_get_totalacdcalltime","tapi3cc/ITAgent::get_TotalACDCallTime"]
old-location: tapi3\itagent_get_totalacdcalltime.htm
tech.root: tapi3
ms.assetid: 432e22b7-16c3-447d-bbec-59ab7713039c
ms.date: 08/10/2022
ms.keywords: ITAgent interface [TAPI 2.2],get_TotalACDCallTime method, ITAgent.get_TotalACDCallTime, ITAgent::get_TotalACDCallTime, _tapi3_itagent_get_totalacdcalltime, get_TotalACDCallTime, get_TotalACDCallTime method [TAPI 2.2], get_TotalACDCallTime method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_totalacdcalltime, tapi3cc/ITAgent::get_TotalACDCallTime
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
 - ITAgent::get_TotalACDCallTime
 - tapi3cc/ITAgent::get_TotalACDCallTime
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
 - ITAgent.get_TotalACDCallTime
---

# ITAgent::get_TotalACDCallTime


## -description

The 
<b>get_TotalACDCallTime</b> gets the number of seconds spent on ACD calls by this agent (across all sessions). This value includes the time spent on the phone plus wrap-up time.

The measurement period over which this information is calculated is switch- and/or implementation-specific. (See 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-get_measurementperiod">get_MeasurementPeriod</a>.)

## -parameters

### -param plCallTime [out]

Total call time.

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
The <i>plCallTime</i> parameter is not a valid pointer.

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
