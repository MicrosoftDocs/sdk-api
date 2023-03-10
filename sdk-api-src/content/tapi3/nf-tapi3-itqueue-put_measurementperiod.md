---
UID: NF:tapi3.ITQueue.put_MeasurementPeriod
title: ITQueue::put_MeasurementPeriod (tapi3.h)
description: The ITQueue::put_MeasurementPeriod (tapi3.h) method sets the period (in seconds) for which the switch and/or implementation stores and calculates information.
helpviewer_keywords: ["ITQueue interface [TAPI 2.2]","put_MeasurementPeriod method","ITQueue.put_MeasurementPeriod","ITQueue::put_MeasurementPeriod","_tapi3_itqueue_put_measurementperiod","put_MeasurementPeriod","put_MeasurementPeriod method [TAPI 2.2]","put_MeasurementPeriod method [TAPI 2.2]","ITQueue interface","tapi3.itqueue_put_measurementperiod","tapi3cc/ITQueue::put_MeasurementPeriod"]
old-location: tapi3\itqueue_put_measurementperiod.htm
tech.root: tapi3
ms.assetid: 9e32b2ae-c4e5-4624-b970-673c950dee3b
ms.date: 08/10/2022
ms.keywords: ITQueue interface [TAPI 2.2],put_MeasurementPeriod method, ITQueue.put_MeasurementPeriod, ITQueue::put_MeasurementPeriod, _tapi3_itqueue_put_measurementperiod, put_MeasurementPeriod, put_MeasurementPeriod method [TAPI 2.2], put_MeasurementPeriod method [TAPI 2.2],ITQueue interface, tapi3.itqueue_put_measurementperiod, tapi3cc/ITQueue::put_MeasurementPeriod
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
 - ITQueue::put_MeasurementPeriod
 - tapi3/ITQueue::put_MeasurementPeriod
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
 - ITQueue.put_MeasurementPeriod
---

# ITQueue::put_MeasurementPeriod


## -description

The 
<b>put_MeasurementPeriod</b> method sets the period (in seconds) for which the switch and/or implementation stores and calculates information.

## -parameters

### -param lPeriod [in]

Measurement period (in seconds).

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Value of <i>lPeriod</i> is zero.

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
<tr>
<td width="40%">
<dl>
<dt><b>LINEERR_</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetqueuemeasurementperiod">lineSetQueueMeasurementPeriod</a> for error codes returned from this TAPI 2.1 function.

</td>
</tr>
</table>

## -remarks

The <b>ITQueue::put_MeasurementPeriod</b> method is a COM wrapper for the TAPI 2.1 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetqueuemeasurementperiod">lineSetQueueMeasurementPeriod</a> function.

This method will accept negative values for the measurement period, but this will normally result in unreliable statistics.

## -see-also

<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_measurementperiod">get_MeasurementPeriod</a>
