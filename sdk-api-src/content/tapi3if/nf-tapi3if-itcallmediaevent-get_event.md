---
UID: NF:tapi3if.ITCallMediaEvent.get_Event
title: ITCallMediaEvent::get_Event (tapi3if.h)
description: The get_Event method gets the call media event indicator.
helpviewer_keywords: ["ITCallMediaEvent interface [TAPI 2.2]","get_Event method","ITCallMediaEvent.get_Event","ITCallMediaEvent::get_Event","_tapi3_itcallmediaevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITCallMediaEvent interface","tapi3.itcallmediaevent_get_event","tapi3if/ITCallMediaEvent::get_Event"]
old-location: tapi3\itcallmediaevent_get_event.htm
tech.root: tapi3
ms.assetid: 3dd6210f-e904-46c5-8fc3-50a62b8754ed
ms.date: 12/05/2018
ms.keywords: ITCallMediaEvent interface [TAPI 2.2],get_Event method, ITCallMediaEvent.get_Event, ITCallMediaEvent::get_Event, _tapi3_itcallmediaevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITCallMediaEvent interface, tapi3.itcallmediaevent_get_event, tapi3if/ITCallMediaEvent::get_Event
f1_keywords:
- tapi3if/ITCallMediaEvent.get_Event
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITCallMediaEvent.get_Event
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallMediaEvent::get_Event


## -description


The 
<b>get_Event</b> method gets the call media event indicator.


## -parameters




### -param pCallMediaEvent [out]

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event">CALL_MEDIA_EVENT</a> indicator.


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
The <i>pCallMediaEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



Call media events are a crucial indicator of whether certain operations can be performed. For example, when 
<b>IVideoWindow</b> is exposed on the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal object</a>, until the CME_STREAM_ACTIVE is received only the 
<b>put_Visible</b> method will succeed. For more information about <b>IVideoWindow</b> and <b>put_Visible</b>, see the DirectX documentation. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event">CALL_MEDIA_EVENT</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent">ITCallMediaEvent</a>
 

 

