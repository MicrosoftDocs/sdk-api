---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITAgent::put_MeasurementPeriod


## -description


The 
<b>put_MeasurementPeriod</b> method sets the period (in seconds) for which the switch and/or implementation stores and calculates information. This also resets any cumulative counts to zero.


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
<dt><b>LINEERR_</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="https://msdn.microsoft.com/bb84f18f-0052-45f8-8049-8576e1eb6fef">lineSetAgentMeasurementPeriod</a> for error codes returned from this TAPI 2.1 function.

</td>
</tr>
</table>
 




## -remarks



The <b>ITAgent::put_MeasurementPeriod</b> method is a COM wrapper for the TAPI 2.1 
<a href="https://msdn.microsoft.com/bb84f18f-0052-45f8-8049-8576e1eb6fef">lineSetAgentMeasurementPeriod</a> function.

This method will accept negative values for the measurement period, but this will normally result in unreliable statistics.




## -see-also




<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<a href="https://msdn.microsoft.com/ccc91dfb-83e5-496a-921d-784fcaea5af5">get_MeasurementPeriod</a>
 

 

