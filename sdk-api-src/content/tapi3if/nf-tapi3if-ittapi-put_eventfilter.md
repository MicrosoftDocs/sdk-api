---
UID: NF:tapi3if.ITTAPI.put_EventFilter
title: ITTAPI::put_EventFilter (tapi3if.h)
description: The put_EventFilter method sets the event filter mask. The mask is a series of ORed members of the TAPI_EVENT enumeration.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","put_EventFilter method","ITTAPI.put_EventFilter","ITTAPI::put_EventFilter","_tapi3_ittapi_put_eventfilter","put_EventFilter","put_EventFilter method [TAPI 2.2]","put_EventFilter method [TAPI 2.2]","ITTAPI interface","tapi3.ittapi_put_eventfilter","tapi3if/ITTAPI::put_EventFilter"]
old-location: tapi3\ittapi_put_eventfilter.htm
tech.root: tapi3
ms.assetid: 126ec551-aade-47d8-987f-1f735f10bd28
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],put_EventFilter method, ITTAPI.put_EventFilter, ITTAPI::put_EventFilter, _tapi3_ittapi_put_eventfilter, put_EventFilter, put_EventFilter method [TAPI 2.2], put_EventFilter method [TAPI 2.2],ITTAPI interface, tapi3.ittapi_put_eventfilter, tapi3if/ITTAPI::put_EventFilter
req.header: tapi3if.h
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
 - ITTAPI::put_EventFilter
 - tapi3if/ITTAPI::put_EventFilter
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
 - ITTAPI.put_EventFilter
---

# ITTAPI::put_EventFilter


## -description

The 
<b>put_EventFilter</b> method sets the event filter mask. The mask is a series of ORed members of the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> enumeration.
<div class="alert"><b>Note</b>  You must call this method to enable reception of events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events.</div><div> </div>

## -parameters

### -param lFilterMask [in]

Event filter mask.

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
</table>

## -see-also

<a href="/windows/desktop/Tapi/events">Events overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapieventnotification">ITTAPIEventNotification</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_eventfilter">get_EventFilter</a>