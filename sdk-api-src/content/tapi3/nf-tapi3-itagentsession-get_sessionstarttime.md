---
UID: NF:tapi3.ITAgentSession.get_SessionStartTime
title: ITAgentSession::get_SessionStartTime
author: windows-sdk-content
description: The get_SessionStartTime method gets the time that the session was created.
old-location: tapi3\itagentsession_get_sessionstarttime.htm
old-project: tapi
ms.assetid: 84c73a96-9748-430f-8653-55656eadc617
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAgentSession interface [TAPI 2.2],get_SessionStartTime method, ITAgentSession.get_SessionStartTime, ITAgentSession::get_SessionStartTime, _tapi3_itagentsession_get_sessionstarttime, get_SessionStartTime, get_SessionStartTime method [TAPI 2.2], get_SessionStartTime method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_sessionstarttime, tapi3cc/ITAgentSession::get_SessionStartTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3.h
req.include-header: Tapi3.h
req.redist: 
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
 - ITAgentSession.get_SessionStartTime
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentSession::get_SessionStartTime


## -description


The 
<b>get_SessionStartTime</b> method gets the time that the session was created.


## -parameters




### -param pdateSessionStart [out]

Pointer to session start time.


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
The <i>pdateSessionStart</i> parameter is not a valid pointer.

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
 

 

