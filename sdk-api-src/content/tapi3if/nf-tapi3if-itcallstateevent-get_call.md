---
UID: NF:tapi3if.ITCallStateEvent.get_Call
title: ITCallStateEvent::get_Call (tapi3if.h)
description: The get_Call method gets a pointer to the call information interface for the call on which the event has occurred. (ITCallStateEvent.get_Call)
helpviewer_keywords: ["ITCallStateEvent interface [TAPI 2.2]","get_Call method","ITCallStateEvent.get_Call","ITCallStateEvent::get_Call","_tapi3_itcallstateevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITCallStateEvent interface","tapi3.itcallstateevent_get_call","tapi3if/ITCallStateEvent::get_Call"]
old-location: tapi3\itcallstateevent_get_call.htm
tech.root: tapi3
ms.assetid: 942bd437-77d1-4d06-91d3-138b06f3228e
ms.date: 12/05/2018
ms.keywords: ITCallStateEvent interface [TAPI 2.2],get_Call method, ITCallStateEvent.get_Call, ITCallStateEvent::get_Call, _tapi3_itcallstateevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITCallStateEvent interface, tapi3.itcallstateevent_get_call, tapi3if/ITCallStateEvent::get_Call
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
 - ITCallStateEvent::get_Call
 - tapi3if/ITCallStateEvent::get_Call
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
 - ITCallStateEvent.get_Call
---

# ITCallStateEvent::get_Call


## -description

The 
<b>get_Call</b> method gets a pointer to the call information interface for the call on which the event has occurred.

## -parameters

### -param ppCallInfo [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCallInfo</i> parameter is not a valid pointer.

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

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent">ITCallStateEvent</a>
