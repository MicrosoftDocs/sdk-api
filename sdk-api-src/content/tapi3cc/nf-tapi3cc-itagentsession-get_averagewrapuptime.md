---
UID: NF:tapi3cc.ITAgentSession.get_AverageWrapUpTime
title: ITAgentSession::get_AverageWrapUpTime (tapi3cc.h)
description: The ITAgentSession::get_AverageWrapUpTime method (tapi3cc.h) gets the average time (in seconds) per ACD call spent in wrap-up during this agent session.
helpviewer_keywords: ["ITAgentSession interface [TAPI 2.2]","get_AverageWrapUpTime method","ITAgentSession.get_AverageWrapUpTime","ITAgentSession::get_AverageWrapUpTime","_tapi3_itagentsession_get_averagewrapuptime","get_AverageWrapUpTime","get_AverageWrapUpTime method [TAPI 2.2]","get_AverageWrapUpTime method [TAPI 2.2]","ITAgentSession interface","tapi3.itagentsession_get_averagewrapuptime","tapi3cc/ITAgentSession::get_AverageWrapUpTime"]
old-location: tapi3\itagentsession_get_averagewrapuptime.htm
tech.root: tapi3
ms.assetid: 365d98ab-9127-45bb-8232-3e3903bd9ab3
ms.date: 08/10/2022
ms.keywords: ITAgentSession interface [TAPI 2.2],get_AverageWrapUpTime method, ITAgentSession.get_AverageWrapUpTime, ITAgentSession::get_AverageWrapUpTime, _tapi3_itagentsession_get_averagewrapuptime, get_AverageWrapUpTime, get_AverageWrapUpTime method [TAPI 2.2], get_AverageWrapUpTime method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_averagewrapuptime, tapi3cc/ITAgentSession::get_AverageWrapUpTime
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
 - ITAgentSession::get_AverageWrapUpTime
 - tapi3cc/ITAgentSession::get_AverageWrapUpTime
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
 - ITAgentSession.get_AverageWrapUpTime
---

# ITAgentSession::get_AverageWrapUpTime


## -description

The 
<b>get_AverageWrapUpTime</b> method gets the average time (in seconds) per ACD call spent in wrap-up (after-call work) during this agent session.

## -parameters

### -param plWrapUpTime [out]

Pointer to average wrap-up time.

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
