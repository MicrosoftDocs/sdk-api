---
UID: NF:tapi3.ITAgent.get_TotalACDCallTime
title: ITAgent::get_TotalACDCallTime
author: windows-sdk-content
description: The get_TotalACDCallTime gets the number of seconds spent on ACD calls by this agent (across all sessions). This value includes the time spent on the phone plus wrap-up time.
old-location: tapi3\itagent_get_totalacdcalltime.htm
tech.root: Tapi
ms.assetid: 432e22b7-16c3-447d-bbec-59ab7713039c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITAgent interface [TAPI 2.2],get_TotalACDCallTime method, ITAgent.get_TotalACDCallTime, ITAgent::get_TotalACDCallTime, _tapi3_itagent_get_totalacdcalltime, get_TotalACDCallTime, get_TotalACDCallTime method [TAPI 2.2], get_TotalACDCallTime method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_totalacdcalltime, tapi3cc/ITAgent::get_TotalACDCallTime
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgent.get_TotalACDCallTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgent::get_TotalACDCallTime


## -description


The 
<b>get_TotalACDCallTime</b> gets the number of seconds spent on ACD calls by this agent (across all sessions). This value includes the time spent on the phone plus wrap-up time.

The measurement period over which this information is calculated is switch- and/or implementation-specific. (See 
<a href="https://msdn.microsoft.com/ccc91dfb-83e5-496a-921d-784fcaea5af5">get_MeasurementPeriod</a>.)


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




<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>
 

 

