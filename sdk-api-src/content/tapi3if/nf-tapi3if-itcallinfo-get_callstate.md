---
UID: NF:tapi3if.ITCallInfo.get_CallState
title: ITCallInfo::get_CallState (tapi3if.h)
description: The get_CallState method gets a pointer to the current call state, such as CS_IDLE.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","get_CallState method","ITCallInfo.get_CallState","ITCallInfo::get_CallState","_tapi3_itcallinfo_get_callstate","get_CallState","get_CallState method [TAPI 2.2]","get_CallState method [TAPI 2.2]","ITCallInfo interface","tapi3.itcallinfo_get_callstate","tapi3if/ITCallInfo::get_CallState"]
old-location: tapi3\itcallinfo_get_callstate.htm
tech.root: tapi3
ms.assetid: f7beb48f-d7d2-4a99-8e6a-6122059c9170
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_CallState method, ITCallInfo.get_CallState, ITCallInfo::get_CallState, _tapi3_itcallinfo_get_callstate, get_CallState, get_CallState method [TAPI 2.2], get_CallState method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_callstate, tapi3if/ITCallInfo::get_CallState
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
 - ITCallInfo::get_CallState
 - tapi3if/ITCallInfo::get_CallState
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
 - ITCallInfo.get_CallState
---

# ITCallInfo::get_CallState


## -description

The 
<b>get_CallState</b> method gets a pointer to the current 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">call state</a>, such as CS_IDLE.

## -parameters

### -param pCallState [out]

Pointer to variable containing current 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">CALL_STATE</a> type.

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
The <i>pCallState</i> parameter is not a valid pointer.

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

## -remarks

<b>TAPI 2.1 Cross-References:  </b><a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a>, <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>, <b>dwMediaMode</b> member of <a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure, <a href="/windows/desktop/Tapi/call-object">Call Object</a>

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">CALL_STATE</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>