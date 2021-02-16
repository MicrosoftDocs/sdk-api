---
UID: NF:tapi3if.ITCallMediaEvent.get_Stream
title: ITCallMediaEvent::get_Stream (tapi3if.h)
description: The get_Stream method gets a pointer to the ITStream interface associated with the call media event.
helpviewer_keywords: ["ITCallMediaEvent interface [TAPI 2.2]","get_Stream method","ITCallMediaEvent.get_Stream","ITCallMediaEvent::get_Stream","_tapi3_itcallmediaevent_get_stream","get_Stream","get_Stream method [TAPI 2.2]","get_Stream method [TAPI 2.2]","ITCallMediaEvent interface","tapi3.itcallmediaevent_get_stream","tapi3if/ITCallMediaEvent::get_Stream"]
old-location: tapi3\itcallmediaevent_get_stream.htm
tech.root: tapi3
ms.assetid: 2afcb8ee-1f8c-41d0-8a8f-f34ebf09d224
ms.date: 12/05/2018
ms.keywords: ITCallMediaEvent interface [TAPI 2.2],get_Stream method, ITCallMediaEvent.get_Stream, ITCallMediaEvent::get_Stream, _tapi3_itcallmediaevent_get_stream, get_Stream, get_Stream method [TAPI 2.2], get_Stream method [TAPI 2.2],ITCallMediaEvent interface, tapi3.itcallmediaevent_get_stream, tapi3if/ITCallMediaEvent::get_Stream
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
 - ITCallMediaEvent::get_Stream
 - tapi3if/ITCallMediaEvent::get_Stream
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
 - ITCallMediaEvent.get_Stream
---

# ITCallMediaEvent::get_Stream


## -description

The 
<b>get_Stream</b> method gets a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface associated with the call media event.

## -parameters

### -param ppStream [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface pointer.

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
The <i>ppStream</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface returned by <b>ITCallMediaEvent::get_Stream</b>. The application must call <b>Release</b> on 
<b>ITStream</b> to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent">ITCallMediaEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>