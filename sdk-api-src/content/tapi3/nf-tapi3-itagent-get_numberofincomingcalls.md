---
UID: NF:tapi3.ITAgent.get_NumberOfIncomingCalls
title: ITAgent::get_NumberOfIncomingCalls method
author: windows-driver-content
description: The get_NumberOfIncomingCalls method gets the number of incoming non-ACD calls handled by this agent.
old-location: tapi3\itagent_get_numberofincomingcalls.htm
old-project: Tapi
ms.assetid: d70073e9-a181-4f8d-b34f-95c8a24fe8d6
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITAgent, ITAgent interface [TAPI 2.2], get_NumberOfIncomingCalls method, ITAgent::get_NumberOfIncomingCalls, _tapi3_itagent_get_numberofincomingcalls, get_NumberOfIncomingCalls method [TAPI 2.2], get_NumberOfIncomingCalls method [TAPI 2.2], ITAgent interface, get_NumberOfIncomingCalls,ITAgent.get_NumberOfIncomingCalls, tapi3.itagent_get_numberofincomingcalls, tapi3cc/ITAgent::get_NumberOfIncomingCalls
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
-	ITAgent.get_NumberOfIncomingCalls
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgent::get_NumberOfIncomingCalls method


## -description


The 
<b>get_NumberOfIncomingCalls</b> method gets the number of incoming non-ACD calls handled by this agent.

The measurement period over which this information is calculated is switch- and/or implementation-specific. (See 
<a href="https://msdn.microsoft.com/ccc91dfb-83e5-496a-921d-784fcaea5af5">get_MeasurementPeriod</a>.)


## -parameters




### -param plCalls [out]

Total number of incoming calls.


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
The <i>plCalls</i> parameter is not a valid pointer.

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
 

 

