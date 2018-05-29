---
UID: NF:tapi3cc.ITAgent.get_TotalACDTalkTime
title: ITAgent::get_TotalACDTalkTime
author: windows-sdk-content
description: The get_TotalACDTalkTime gets the number of seconds spent talking in ACD calls by this agent (across all sessions).
old-location: tapi3\itagent_get_totalacdtalktime.htm
old-project: Tapi
ms.assetid: a622a812-c929-413a-a3bc-4e870158cf16
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITAgent interface [TAPI 2.2],get_TotalACDTalkTime method, ITAgent.get_TotalACDTalkTime, ITAgent::get_TotalACDTalkTime, _tapi3_itagent_get_totalacdtalktime, get_TotalACDTalkTime, get_TotalACDTalkTime method [TAPI 2.2], get_TotalACDTalkTime method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_totalacdtalktime, tapi3cc/ITAgent::get_TotalACDTalkTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: AGENT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITAgent.get_TotalACDTalkTime
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgent::get_TotalACDTalkTime


## -description


The 
<b>get_TotalACDTalkTime</b> gets the number of seconds spent talking in ACD calls by this agent (across all sessions).

The measurement period over which this information is calculated is switch- and/or implementation-specific. (See 
<a href="https://msdn.microsoft.com/ccc91dfb-83e5-496a-921d-784fcaea5af5">get_MeasurementPeriod</a>.)


## -parameters




### -param plTalkTime [out]

Total talk time.


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
The <i>plTalkTime</i> parameter is not a valid pointer.

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
 

 

