---
UID: NF:tapi3if.ITCallStateEvent.get_Cause
title: ITCallStateEvent::get_Cause (tapi3if.h)
description: The get_Cause method gets the cause associated with this event. (ITCallStateEvent.get_Cause)
helpviewer_keywords: ["ITCallStateEvent interface [TAPI 2.2]","get_Cause method","ITCallStateEvent.get_Cause","ITCallStateEvent::get_Cause","_tapi3_itcallstateevent_get_cause","get_Cause","get_Cause method [TAPI 2.2]","get_Cause method [TAPI 2.2]","ITCallStateEvent interface","tapi3.itcallstateevent_get_cause","tapi3if/ITCallStateEvent::get_Cause"]
old-location: tapi3\itcallstateevent_get_cause.htm
tech.root: tapi3
ms.assetid: e3a4b985-1c0f-4e93-a965-c61c9c0ab10d
ms.date: 12/05/2018
ms.keywords: ITCallStateEvent interface [TAPI 2.2],get_Cause method, ITCallStateEvent.get_Cause, ITCallStateEvent::get_Cause, _tapi3_itcallstateevent_get_cause, get_Cause, get_Cause method [TAPI 2.2], get_Cause method [TAPI 2.2],ITCallStateEvent interface, tapi3.itcallstateevent_get_cause, tapi3if/ITCallStateEvent::get_Cause
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
 - ITCallStateEvent::get_Cause
 - tapi3if/ITCallStateEvent::get_Cause
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
 - ITCallStateEvent.get_Cause
---

# ITCallStateEvent::get_Cause


## -description

The 
<b>get_Cause</b> method gets the cause associated with this event.

## -parameters

### -param pCEC [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state_event_cause">CALL_STATE_EVENT_CAUSE</a> indicator.

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
The <i>pCEC</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state_event_cause">CALL_STATE_EVENT_CAUSE</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent">ITCallStateEvent</a>
