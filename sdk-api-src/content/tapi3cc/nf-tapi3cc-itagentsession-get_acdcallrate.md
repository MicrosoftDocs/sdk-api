---
UID: NF:tapi3cc.ITAgentSession.get_ACDCallRate
title: ITAgentSession::get_ACDCallRate (tapi3cc.h)
description: The ITAgentSession::get_ACDCallRate method (tapi3cc.h) gets the all rate per agent session, in calls per hour.
helpviewer_keywords: ["ITAgentSession interface [TAPI 2.2]","get_ACDCallRate method","ITAgentSession.get_ACDCallRate","ITAgentSession::get_ACDCallRate","_tapi3_itagentsession_get_acdcallrate","get_ACDCallRate","get_ACDCallRate method [TAPI 2.2]","get_ACDCallRate method [TAPI 2.2]","ITAgentSession interface","tapi3.itagentsession_get_acdcallrate","tapi3cc/ITAgentSession::get_ACDCallRate"]
old-location: tapi3\itagentsession_get_acdcallrate.htm
tech.root: tapi3
ms.assetid: 49737945-7e27-4c88-94c5-29db7dccfc97
ms.date: 08/10/2022
ms.keywords: ITAgentSession interface [TAPI 2.2],get_ACDCallRate method, ITAgentSession.get_ACDCallRate, ITAgentSession::get_ACDCallRate, _tapi3_itagentsession_get_acdcallrate, get_ACDCallRate, get_ACDCallRate method [TAPI 2.2], get_ACDCallRate method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_acdcallrate, tapi3cc/ITAgentSession::get_ACDCallRate
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
 - ITAgentSession::get_ACDCallRate
 - tapi3cc/ITAgentSession::get_ACDCallRate
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
 - ITAgentSession.get_ACDCallRate
---

# ITAgentSession::get_ACDCallRate


## -description

The 
<b>get_ACDCallRate</b> method gets the all rate per agent session, in calls per hour.

## -parameters

### -param pcyCallrate [out]

Pointer to call rate.

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
The <i>pcyCallrate</i> parameter is not a valid pointer.

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
