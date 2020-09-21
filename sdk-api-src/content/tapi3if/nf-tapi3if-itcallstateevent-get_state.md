---
UID: NF:tapi3if.ITCallStateEvent.get_State
title: ITCallStateEvent::get_State (tapi3if.h)
description: The get_State method gets information on the new call state.
helpviewer_keywords: ["ITCallStateEvent interface [TAPI 2.2]","get_State method","ITCallStateEvent.get_State","ITCallStateEvent::get_State","_tapi3_itcallstateevent_get_state","get_State","get_State method [TAPI 2.2]","get_State method [TAPI 2.2]","ITCallStateEvent interface","tapi3.itcallstateevent_get_state","tapi3if/ITCallStateEvent::get_State"]
old-location: tapi3\itcallstateevent_get_state.htm
tech.root: tapi3
ms.assetid: 45e46b99-c65f-4296-9537-7fb7a4210727
ms.date: 12/05/2018
ms.keywords: ITCallStateEvent interface [TAPI 2.2],get_State method, ITCallStateEvent.get_State, ITCallStateEvent::get_State, _tapi3_itcallstateevent_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITCallStateEvent interface, tapi3.itcallstateevent_get_state, tapi3if/ITCallStateEvent::get_State
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
 - ITCallStateEvent::get_State
 - tapi3if/ITCallStateEvent::get_State
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
 - ITCallStateEvent.get_State
---

# ITCallStateEvent::get_State


## -description

The 
<b>get_State</b> method gets information on the new call state.

## -parameters

### -param pCallState [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">CALL_STATE</a> constant.

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
The <i>pCallState</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">CALL_STATE</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent">ITCallStateEvent</a>