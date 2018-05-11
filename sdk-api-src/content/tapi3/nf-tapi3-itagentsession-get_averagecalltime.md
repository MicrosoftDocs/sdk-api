---
UID: NF:tapi3.ITAgentSession.get_AverageCallTime
title: ITAgentSession::get_AverageCallTime
author: windows-driver-content
description: The get_AverageCallTime method gets the average time (in seconds) spent per ACD call during this agent session. This value includes the time spent on the phone plus wrap-up time.
old-location: tapi3\itagentsession_get_averagecalltime.htm
old-project: Tapi
ms.assetid: 05029076-cb76-4771-b0a8-0c09e184e6ee
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITAgentSession interface [TAPI 2.2],get_AverageCallTime method, ITAgentSession.get_AverageCallTime, ITAgentSession::get_AverageCallTime, _tapi3_itagentsession_get_averagecalltime, get_AverageCallTime, get_AverageCallTime method [TAPI 2.2], get_AverageCallTime method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_averagecalltime, tapi3cc/ITAgentSession::get_AverageCallTime
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
-	ITAgentSession.get_AverageCallTime
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentSession::get_AverageCallTime


## -description


The 
<b>get_AverageCallTime</b> method gets the average time (in seconds) spent per ACD call during this agent session. This value includes the time spent on the phone plus wrap-up time.


## -parameters




### -param plCallTime [out]

Pointer to the average call time.


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
<dt><b>LINEERR_</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="https://msdn.microsoft.com/06a5ea23-4205-46fd-abe7-ee4575be81c8">lineGetAgentSessionInfo</a> for error codes returned from this TAPI 2.1 function.

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



This method wraps the TAPI 2.1 
<a href="https://msdn.microsoft.com/06a5ea23-4205-46fd-abe7-ee4575be81c8">lineGetAgentSessionInfo</a> function.




## -see-also




<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>



<a href="https://msdn.microsoft.com/06a5ea23-4205-46fd-abe7-ee4575be81c8">lineGetAgentSessionInfo</a>
 

 

