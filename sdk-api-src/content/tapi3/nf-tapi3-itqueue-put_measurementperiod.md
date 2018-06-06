---
UID: NF:tapi3.ITQueue.put_MeasurementPeriod
title: ITQueue::put_MeasurementPeriod
author: windows-sdk-content
description: The put_MeasurementPeriod method sets the period (in seconds) for which the switch and/or implementation stores and calculates information.
old-location: tapi3\itqueue_put_measurementperiod.htm
old-project: Tapi
ms.assetid: 9e32b2ae-c4e5-4624-b970-673c950dee3b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITQueue interface [TAPI 2.2],put_MeasurementPeriod method, ITQueue.put_MeasurementPeriod, ITQueue::put_MeasurementPeriod, _tapi3_itqueue_put_measurementperiod, put_MeasurementPeriod, put_MeasurementPeriod method [TAPI 2.2], put_MeasurementPeriod method [TAPI 2.2],ITQueue interface, tapi3.itqueue_put_measurementperiod, tapi3cc/ITQueue::put_MeasurementPeriod
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
 - ITQueue.put_MeasurementPeriod
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="https://msdn.microsoft.com/62b972ed-4a2d-4756-b905-dfb8c2bb0a8c">lineSetQueueMeasurementPeriod</a> for error codes returned from this TAPI 2.1 function.

</td>
</tr>
</table>
 




## -remarks



The <b>ITQueue::put_MeasurementPeriod</b> method is a COM wrapper for the TAPI 2.1 
<a href="https://msdn.microsoft.com/62b972ed-4a2d-4756-b905-dfb8c2bb0a8c">lineSetQueueMeasurementPeriod</a> function.

This method will accept negative values for the measurement period, but this will normally result in unreliable statistics.




## -see-also




<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a>



<a href="https://msdn.microsoft.com/931fb7dd-8c9b-4b1e-9296-6335e5a7e164">get_MeasurementPeriod</a>
 

 

