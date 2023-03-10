---
UID: NF:tapi3cc.ITQueue.get_AverageWaitTime
title: ITQueue::get_AverageWaitTime (tapi3cc.h)
description: The ITQueue::get_AverageWaitTime method (tapi3cc.h) gets the average time in the queue (in seconds) for a call during the current measurement period.
helpviewer_keywords: ["ITQueue interface [TAPI 2.2]","get_AverageWaitTime method","ITQueue.get_AverageWaitTime","ITQueue::get_AverageWaitTime","_tapi3_itqueue_get_averagewaittime","get_AverageWaitTime","get_AverageWaitTime method [TAPI 2.2]","get_AverageWaitTime method [TAPI 2.2]","ITQueue interface","tapi3.itqueue_get_averagewaittime","tapi3cc/ITQueue::get_AverageWaitTime"]
old-location: tapi3\itqueue_get_averagewaittime.htm
tech.root: tapi3
ms.assetid: 94883656-8a72-464d-9478-89f698c98db8
ms.date: 08/10/2022
ms.keywords: ITQueue interface [TAPI 2.2],get_AverageWaitTime method, ITQueue.get_AverageWaitTime, ITQueue::get_AverageWaitTime, _tapi3_itqueue_get_averagewaittime, get_AverageWaitTime, get_AverageWaitTime method [TAPI 2.2], get_AverageWaitTime method [TAPI 2.2],ITQueue interface, tapi3.itqueue_get_averagewaittime, tapi3cc/ITQueue::get_AverageWaitTime
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
 - ITQueue::get_AverageWaitTime
 - tapi3cc/ITQueue::get_AverageWaitTime
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
 - ITQueue.get_AverageWaitTime
---

# ITQueue::get_AverageWaitTime


## -description

The 
<b>get_AverageWaitTime</b> method gets the average time in the queue (in seconds) for a call during the current measurement period. The measurement period is switch or implementation specific. (See 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_measurementperiod">get_MeasurementPeriod</a>.)

## -parameters

### -param plWaitTime [out]

Pointer to the average wait time.

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
The <i>plWaitTime</i> is not a valid pointer.

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
