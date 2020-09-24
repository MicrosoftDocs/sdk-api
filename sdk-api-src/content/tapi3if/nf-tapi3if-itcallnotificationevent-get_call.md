---
UID: NF:tapi3if.ITCallNotificationEvent.get_Call
title: ITCallNotificationEvent::get_Call (tapi3if.h)
description: The get_Call method returns the ITCallInfo interface on which a call event has occurred.
helpviewer_keywords: ["ITCallNotificationEvent interface [TAPI 2.2]","get_Call method","ITCallNotificationEvent.get_Call","ITCallNotificationEvent::get_Call","_tapi3_itcallnotificationevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITCallNotificationEvent interface","tapi3.itcallnotificationevent_get_call","tapi3if/ITCallNotificationEvent::get_Call"]
old-location: tapi3\itcallnotificationevent_get_call.htm
tech.root: tapi3
ms.assetid: 6ff82bd1-de69-4ab7-9152-a578b8566755
ms.date: 12/05/2018
ms.keywords: ITCallNotificationEvent interface [TAPI 2.2],get_Call method, ITCallNotificationEvent.get_Call, ITCallNotificationEvent::get_Call, _tapi3_itcallnotificationevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITCallNotificationEvent interface, tapi3.itcallnotificationevent_get_call, tapi3if/ITCallNotificationEvent::get_Call
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
 - ITCallNotificationEvent::get_Call
 - tapi3if/ITCallNotificationEvent::get_Call
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
 - ITCallNotificationEvent.get_Call
---

# ITCallNotificationEvent::get_Call


## -description

The 
<b>get_Call</b> method returns the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface on which a call event has occurred.

## -parameters

### -param ppCall [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface on which call event has occurred.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>ppCall</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface returned by <b>ITCallNotificationEvent::get_Call</b>. The application must call <b>Release</b> on 
<b>ITCallInfo</b> to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>