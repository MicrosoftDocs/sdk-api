---
UID: NF:tapi3if.ITQOSEvent.get_Call
title: ITQOSEvent::get_Call (tapi3if.h)
description: The get_Call method gets a pointer to the ITCallInfo interface for the call on which the QOS event occurred.
helpviewer_keywords: ["ITQOSEvent interface [TAPI 2.2]","get_Call method","ITQOSEvent.get_Call","ITQOSEvent::get_Call","_tapi3_itqosevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITQOSEvent interface","tapi3.itqosevent_get_call","tapi3if/ITQOSEvent::get_Call"]
old-location: tapi3\itqosevent_get_call.htm
tech.root: tapi3
ms.assetid: e91772da-948a-4d0a-999e-cdd51951fca2
ms.date: 12/05/2018
ms.keywords: ITQOSEvent interface [TAPI 2.2],get_Call method, ITQOSEvent.get_Call, ITQOSEvent::get_Call, _tapi3_itqosevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITQOSEvent interface, tapi3.itqosevent_get_call, tapi3if/ITQOSEvent::get_Call
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
 - ITQOSEvent::get_Call
 - tapi3if/ITQOSEvent::get_Call
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
 - ITQOSEvent.get_Call
---

# ITQOSEvent::get_Call


## -description

The 
<b>get_Call</b> method gets a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface for the call on which the QOS event occurred.

## -parameters

### -param ppCall [out]

Points to 
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCall</i> parameter is not a valid pointer.

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

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface returned by <b>tapi3.itqosevent_get_call</b>. The application must call <b>Release</b> on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent">ITQOSEvent</a>