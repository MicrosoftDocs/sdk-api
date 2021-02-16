---
UID: NF:tapi3if.ITCallMediaEvent.get_Call
title: ITCallMediaEvent::get_Call (tapi3if.h)
description: The get_Call method gets an ITCallInfo interface pointer for the call object associated with this event.
helpviewer_keywords: ["ITCallMediaEvent interface [TAPI 2.2]","get_Call method","ITCallMediaEvent.get_Call","ITCallMediaEvent::get_Call","_tapi3_itcallmediaevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITCallMediaEvent interface","tapi3.itcallmediaevent_get_call","tapi3if/ITCallMediaEvent::get_Call"]
old-location: tapi3\itcallmediaevent_get_call.htm
tech.root: tapi3
ms.assetid: f343c0d2-78bd-415d-9bab-f21a32343119
ms.date: 12/05/2018
ms.keywords: ITCallMediaEvent interface [TAPI 2.2],get_Call method, ITCallMediaEvent.get_Call, ITCallMediaEvent::get_Call, _tapi3_itcallmediaevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITCallMediaEvent interface, tapi3.itcallmediaevent_get_call, tapi3if/ITCallMediaEvent::get_Call
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
 - ITCallMediaEvent::get_Call
 - tapi3if/ITCallMediaEvent::get_Call
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
 - ITCallMediaEvent.get_Call
---

# ITCallMediaEvent::get_Call


## -description

The 
<b>get_Call</b> method gets an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface pointer for the call object associated with this event.

## -parameters

### -param ppCallInfo [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

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
The <i>ppCallInfo</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface returned by <b>ITCallMediaEvent::get_Call</b>. The application must call <b>Release</b> on 
<b>ITCallInfo</b> to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent">ITCallMediaEvent</a>