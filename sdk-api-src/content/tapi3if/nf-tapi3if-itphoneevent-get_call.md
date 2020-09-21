---
UID: NF:tapi3if.ITPhoneEvent.get_Call
title: ITPhoneEvent::get_Call (tapi3if.h)
description: The get_Call method returns a pointer to the ITCallInfo interface for the call object involved in the event.
helpviewer_keywords: ["ITPhoneEvent interface [TAPI 2.2]","get_Call method","ITPhoneEvent.get_Call","ITPhoneEvent::get_Call","_tapi3_itphoneevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITPhoneEvent interface","tapi3.itphoneevent_get_call","tapi3if/ITPhoneEvent::get_Call"]
old-location: tapi3\itphoneevent_get_call.htm
tech.root: tapi3
ms.assetid: 52305981-d97a-4b7c-9886-6e2543bd1a27
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_Call method, ITPhoneEvent.get_Call, ITPhoneEvent::get_Call, _tapi3_itphoneevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_call, tapi3if/ITPhoneEvent::get_Call
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
 - ITPhoneEvent::get_Call
 - tapi3if/ITPhoneEvent::get_Call
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
 - ITPhoneEvent.get_Call
---

# ITPhoneEvent::get_Call


## -description

The 
<b>get_Call</b> method returns a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface for the call object involved in the event.

## -parameters

### -param ppCallInfo [out]

 Pointer to the 
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

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>