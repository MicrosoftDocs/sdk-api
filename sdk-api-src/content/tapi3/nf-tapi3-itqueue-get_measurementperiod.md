---
UID: NF:tapi3.ITQueue.get_MeasurementPeriod
title: ITQueue::get_MeasurementPeriod (tapi3.h)
description: The ITQueue::get_MeasurementPeriod (tapi3.h) method gets the measurement period for which the switch and/or implementation stores and calculates information.
helpviewer_keywords: ["ITQueue interface [TAPI 2.2]","get_MeasurementPeriod method","ITQueue.get_MeasurementPeriod","ITQueue::get_MeasurementPeriod","_tapi3_itqueue_get_measurementperiod","get_MeasurementPeriod","get_MeasurementPeriod method [TAPI 2.2]","get_MeasurementPeriod method [TAPI 2.2]","ITQueue interface","tapi3.itqueue_get_measurementperiod","tapi3cc/ITQueue::get_MeasurementPeriod"]
old-location: tapi3\itqueue_get_measurementperiod.htm
tech.root: tapi3
ms.assetid: 931fb7dd-8c9b-4b1e-9296-6335e5a7e164
ms.date: 08/10/2022
ms.keywords: ITQueue interface [TAPI 2.2],get_MeasurementPeriod method, ITQueue.get_MeasurementPeriod, ITQueue::get_MeasurementPeriod, _tapi3_itqueue_get_measurementperiod, get_MeasurementPeriod, get_MeasurementPeriod method [TAPI 2.2], get_MeasurementPeriod method [TAPI 2.2],ITQueue interface, tapi3.itqueue_get_measurementperiod, tapi3cc/ITQueue::get_MeasurementPeriod
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
 - ITQueue::get_MeasurementPeriod
 - tapi3/ITQueue::get_MeasurementPeriod
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
 - ITQueue.get_MeasurementPeriod
---

# ITQueue::get_MeasurementPeriod


## -description

The 
<b>get_MeasurementPeriod</b> method gets the measurement period (in seconds) for which the switch and/or implementation stores and calculates information. For example, the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_totalcallsqueued">get_TotalCallsQueued</a> method returns the number of calls queued; 
<b>get_MeasurementPeriod</b> indicates if this value referenced the calls queued in an hour, a day, a month, etc.

## -parameters

### -param plPeriod [out]

Pointer to the measurement period.

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
The <i>plPeriod</i> is not a valid pointer.

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

<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itqueue-put_measurementperiod">put_MeasurementPeriod</a>
