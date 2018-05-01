---
UID: NF:tapi3.ITQueue.get_MeasurementPeriod
title: ITQueue::get_MeasurementPeriod method
author: windows-driver-content
description: The get_MeasurementPeriod method gets the measurement period (in seconds) for which the switch and/or implementation stores and calculates information.
old-location: tapi3\itqueue_get_measurementperiod.htm
old-project: Tapi
ms.assetid: 931fb7dd-8c9b-4b1e-9296-6335e5a7e164
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITQueue, ITQueue interface [TAPI 2.2], get_MeasurementPeriod method, ITQueue::get_MeasurementPeriod, _tapi3_itqueue_get_measurementperiod, get_MeasurementPeriod method [TAPI 2.2], get_MeasurementPeriod method [TAPI 2.2], ITQueue interface, get_MeasurementPeriod,ITQueue.get_MeasurementPeriod, tapi3.itqueue_get_measurementperiod, tapi3cc/ITQueue::get_MeasurementPeriod
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MSP_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITQueue.get_MeasurementPeriod
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITQueue::get_MeasurementPeriod method


## -description


The 
<b>get_MeasurementPeriod</b> method gets the measurement period (in seconds) for which the switch and/or implementation stores and calculates information. For example, the 
<a href="https://msdn.microsoft.com/45a1a47a-4cbe-47dd-ad48-218e74fe74b4">get_TotalCallsQueued</a> method returns the number of calls queued; 
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




<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a>



<a href="https://msdn.microsoft.com/9e32b2ae-c4e5-4624-b970-673c950dee3b">put_MeasurementPeriod</a>
 

 

