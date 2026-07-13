---
UID: NF:tapi3cc.ITAgentSession.get_SessionStartTime
title: ITAgentSession::get_SessionStartTime (tapi3cc.h)
description: The ITAgentSession::get_SessionStartTime (tapi3cc.h) method gets the time that the session was created.
helpviewer_keywords: ["ITAgentSession interface [TAPI 2.2]","get_SessionStartTime method","ITAgentSession.get_SessionStartTime","ITAgentSession::get_SessionStartTime","_tapi3_itagentsession_get_sessionstarttime","get_SessionStartTime","get_SessionStartTime method [TAPI 2.2]","get_SessionStartTime method [TAPI 2.2]","ITAgentSession interface","tapi3.itagentsession_get_sessionstarttime","tapi3cc/ITAgentSession::get_SessionStartTime"]
old-location: tapi3\itagentsession_get_sessionstarttime.htm
tech.root: tapi3
ms.assetid: 84c73a96-9748-430f-8653-55656eadc617
ms.date: 08/10/2022
ms.keywords: ITAgentSession interface [TAPI 2.2],get_SessionStartTime method, ITAgentSession.get_SessionStartTime, ITAgentSession::get_SessionStartTime, _tapi3_itagentsession_get_sessionstarttime, get_SessionStartTime, get_SessionStartTime method [TAPI 2.2], get_SessionStartTime method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_sessionstarttime, tapi3cc/ITAgentSession::get_SessionStartTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAgentSession::get_SessionStartTime
 - tapi3cc/ITAgentSession::get_SessionStartTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentSession.get_SessionStartTime
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
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a> for error codes returned from this TAPI 2.1 function.

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
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a> function.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a>
