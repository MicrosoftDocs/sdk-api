---
UID: NF:tapi3if.ITTAPI.get_EventFilter
title: ITTAPI::get_EventFilter (tapi3if.h)
description: The get_EventFilter method gets the current event filter mask. The mask is a series of ORed members of the TAPI_EVENT enumeration.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","get_EventFilter method","ITTAPI.get_EventFilter","ITTAPI::get_EventFilter","_tapi3_ittapi_get_eventfilter","get_EventFilter","get_EventFilter method [TAPI 2.2]","get_EventFilter method [TAPI 2.2]","ITTAPI interface","tapi3.ittapi_get_eventfilter","tapi3if/ITTAPI::get_EventFilter"]
old-location: tapi3\ittapi_get_eventfilter.htm
tech.root: tapi3
ms.assetid: c0544e9f-0bfc-43ab-bcf0-800afb0ebfcf
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],get_EventFilter method, ITTAPI.get_EventFilter, ITTAPI::get_EventFilter, _tapi3_ittapi_get_eventfilter, get_EventFilter, get_EventFilter method [TAPI 2.2], get_EventFilter method [TAPI 2.2],ITTAPI interface, tapi3.ittapi_get_eventfilter, tapi3if/ITTAPI::get_EventFilter
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
 - ITTAPI::get_EventFilter
 - tapi3if/ITTAPI::get_EventFilter
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
 - ITTAPI.get_EventFilter
---

# ITTAPI::get_EventFilter


## -description

The 
<b>get_EventFilter</b> method gets the current event filter mask. The mask is a series of ORed members of the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> enumeration.

## -parameters

### -param plFilterMask [out]

Pointer to the event filter mask.

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



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">put_EventFilter</a>