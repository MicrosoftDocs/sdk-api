---
UID: NF:tapi3.ITAgent.get_OverallCallRate
title: ITAgent::get_OverallCallRate
author: windows-sdk-content
description: The get_OverallCallRate method gets an agent's call rate across all sessions. 10 *Calls per agent hour (where agent hour represents the time that an agent was active in one or more agent sessions).
old-location: tapi3\itagent_get_overallcallrate.htm
tech.root: tapi
ms.assetid: ea85f3a7-0081-4ce2-bf2e-c47e6e7c4cbb
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAgent interface [TAPI 2.2],get_OverallCallRate method, ITAgent.get_OverallCallRate, ITAgent::get_OverallCallRate, _tapi3_itagent_get_overallcallrate, get_OverallCallRate, get_OverallCallRate method [TAPI 2.2], get_OverallCallRate method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_overallcallrate, tapi3cc/ITAgent::get_OverallCallRate
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
 - ITAgent.get_OverallCallRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3.h
: 
- ITAgent.get_OverallCallRate
: 
---

# ITAgent::get_OverallCallRate


## -description


The 
<b>get_OverallCallRate</b> method gets an agent's call rate across all sessions. 10 *Calls per agent hour (where agent hour represents the time that an agent was active in one or more agent sessions).

The measurement period over which this information is calculated is switch- and/or implementation-specific. (See 
<a href="https://msdn.microsoft.com/ccc91dfb-83e5-496a-921d-784fcaea5af5">get_MeasurementPeriod</a>.)


## -parameters




### -param pcyCallrate [out]

Call rate.


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
The <i>pcyCallrate</i> parameter is not a valid pointer.

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
 




## -remarks



The <b>CURRENCY</b> type is used here instead of <b>FLOAT</b> for Visual Basic and Java compatibility.




## -see-also




<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>
 

 

