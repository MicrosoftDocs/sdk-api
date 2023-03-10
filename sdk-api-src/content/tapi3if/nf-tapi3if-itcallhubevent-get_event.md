---
UID: NF:tapi3if.ITCallHubEvent.get_Event
title: ITCallHubEvent::get_Event (tapi3if.h)
description: The get_Event method returns a pointer to a CALLHUB_EVENT enum description of the event that occurred.
helpviewer_keywords: ["ITCallHubEvent interface [TAPI 2.2]","get_Event method","ITCallHubEvent.get_Event","ITCallHubEvent::get_Event","_tapi3_itcallhubevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITCallHubEvent interface","tapi3.itcallhubevent_get_event","tapi3if/ITCallHubEvent::get_Event"]
old-location: tapi3\itcallhubevent_get_event.htm
tech.root: tapi3
ms.assetid: a2515583-e564-413d-b93f-6f2dd7776d7b
ms.date: 12/05/2018
ms.keywords: ITCallHubEvent interface [TAPI 2.2],get_Event method, ITCallHubEvent.get_Event, ITCallHubEvent::get_Event, _tapi3_itcallhubevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITCallHubEvent interface, tapi3.itcallhubevent_get_event, tapi3if/ITCallHubEvent::get_Event
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
 - ITCallHubEvent::get_Event
 - tapi3if/ITCallHubEvent::get_Event
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
 - ITCallHubEvent.get_Event
---

# ITCallHubEvent::get_Event


## -description

The 
<b>get_Event</b> method returns a pointer to a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callhub_event">CALLHUB_EVENT</a> enum description of the event that occurred.

## -parameters

### -param pEvent [out]

Pointer to a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callhub_event">CALLHUB_EVENT</a> enum description of the event.

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
The <i>pEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callhub_event">CALLHUB_EVENT</a>



<a href="/windows/desktop/Tapi/callhub-object">CallHub Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent">ITCallHubEvent</a>