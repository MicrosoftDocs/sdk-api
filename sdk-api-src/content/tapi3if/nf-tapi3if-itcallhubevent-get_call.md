---
UID: NF:tapi3if.ITCallHubEvent.get_Call
title: ITCallHubEvent::get_Call (tapi3if.h)
description: The get_Call method returns a pointer to the ITCallInfo interface of the call on which the event occurred.
helpviewer_keywords: ["ITCallHubEvent interface [TAPI 2.2]","get_Call method","ITCallHubEvent.get_Call","ITCallHubEvent::get_Call","_tapi3_itcallhubevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITCallHubEvent interface","tapi3.itcallhubevent_get_call","tapi3if/ITCallHubEvent::get_Call"]
old-location: tapi3\itcallhubevent_get_call.htm
tech.root: tapi3
ms.assetid: 2ac47da3-f60f-41f4-99f7-031744044bd4
ms.date: 12/05/2018
ms.keywords: ITCallHubEvent interface [TAPI 2.2],get_Call method, ITCallHubEvent.get_Call, ITCallHubEvent::get_Call, _tapi3_itcallhubevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITCallHubEvent interface, tapi3.itcallhubevent_get_call, tapi3if/ITCallHubEvent::get_Call
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
 - ITCallHubEvent::get_Call
 - tapi3if/ITCallHubEvent::get_Call
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
 - ITCallHubEvent.get_Call
---

# ITCallHubEvent::get_Call


## -description

The 
<b>get_Call</b> method returns a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface of the call on which the event occurred.

## -parameters

### -param ppCall [out]

<b>ITCallInfo</b> interface.

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
The <i>ppCallt</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

This method may return a <b>NULL</b> if the event is not associated with a call.

## -see-also

<a href="/windows/desktop/Tapi/callhub-object">CallHub Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent">ITCallHubEvent</a>