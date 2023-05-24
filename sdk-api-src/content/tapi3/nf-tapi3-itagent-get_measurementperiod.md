---
UID: NF:tapi3.ITAgent.get_MeasurementPeriod
title: ITAgent::get_MeasurementPeriod (tapi3.h)
description: The get_MeasurementPeriod method (tapi3.h) gets the measurement period for which the switch and/or implementation stores and calculates information.
helpviewer_keywords: ["ITAgent interface [TAPI 2.2]","get_MeasurementPeriod method","ITAgent.get_MeasurementPeriod","ITAgent::get_MeasurementPeriod","_tapi3_itagent_get_measurementperiod","get_MeasurementPeriod","get_MeasurementPeriod method [TAPI 2.2]","get_MeasurementPeriod method [TAPI 2.2]","ITAgent interface","tapi3.itagent_get_measurementperiod","tapi3cc/ITAgent::get_MeasurementPeriod"]
old-location: tapi3\itagent_get_measurementperiod.htm
tech.root: tapi3
ms.assetid: ccc91dfb-83e5-496a-921d-784fcaea5af5
ms.date: 08/09/2022
ms.keywords: ITAgent interface [TAPI 2.2],get_MeasurementPeriod method, ITAgent.get_MeasurementPeriod, ITAgent::get_MeasurementPeriod, _tapi3_itagent_get_measurementperiod, get_MeasurementPeriod, get_MeasurementPeriod method [TAPI 2.2], get_MeasurementPeriod method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_measurementperiod, tapi3cc/ITAgent::get_MeasurementPeriod
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
 - ITAgent::get_MeasurementPeriod
 - tapi3/ITAgent::get_MeasurementPeriod
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
 - ITAgent.get_MeasurementPeriod
---

# ITAgent::get_MeasurementPeriod


## -description

The 
<b>get_MeasurementPeriod</b> method gets the measurement period (in seconds) for which the switch and/or implementation stores and calculates information. For example, 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-get_numberofacdcalls">get_NumberOfACDCalls</a> returns the number of calls the agent handled; 
<b>get_MeasurementPeriod</b> indicates if this value referenced the calls handled in the last hour, day, month, etc.

## -parameters

### -param plPeriod [out]

Measurement period.

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
The <i>plPeriod</i> parameter is not a valid pointer.

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



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-put_measurementperiod">put_MeasurementPeriod</a>
