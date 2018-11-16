---
UID: NF:tapi3cc.ITAgentSession.get_TotalWrapUpTime
title: ITAgentSession::get_TotalWrapUpTime
author: windows-sdk-content
description: The get_TotalWrapUpTime method gets the number of seconds spent on ACD call wrap-up (after-call work) during this agent session (by this agent).
old-location: tapi3\itagentsession_get_totalwrapuptime.htm
tech.root: Tapi
ms.assetid: 5b1cda40-36bd-481a-bc59-81b810ebed09
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITAgentSession interface [TAPI 2.2],get_TotalWrapUpTime method, ITAgentSession.get_TotalWrapUpTime, ITAgentSession::get_TotalWrapUpTime, _tapi3_itagentsession_get_totalwrapuptime, get_TotalWrapUpTime, get_TotalWrapUpTime method [TAPI 2.2], get_TotalWrapUpTime method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_totalwrapuptime, tapi3cc/ITAgentSession::get_TotalWrapUpTime
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITAgentSession.get_TotalWrapUpTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3cc.h
: 
- ITAgentSession.get_TotalWrapUpTime
: 
---

# ITAgentSession::get_TotalWrapUpTime


## -description


The 
<b>get_TotalWrapUpTime</b> method gets the number of seconds spent on ACD call wrap-up (after-call work) during this agent session (by this agent).


## -parameters




### -param plWrapUpTime [out]

Pointer to total wrap-up time.


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
The <i>plWrapUpTime</i> parameter is not a valid pointer.

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
 

 

