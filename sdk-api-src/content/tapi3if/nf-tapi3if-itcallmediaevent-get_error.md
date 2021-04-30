---
UID: NF:tapi3if.ITCallMediaEvent.get_Error
title: ITCallMediaEvent::get_Error (tapi3if.h)
description: The get_Error method gets the error associated with the media event, if any.
helpviewer_keywords: ["ITCallMediaEvent interface [TAPI 2.2]","get_Error method","ITCallMediaEvent.get_Error","ITCallMediaEvent::get_Error","_tapi3_itcallmediaevent_get_error","get_Error","get_Error method [TAPI 2.2]","get_Error method [TAPI 2.2]","ITCallMediaEvent interface","tapi3.itcallmediaevent_get_error","tapi3if/ITCallMediaEvent::get_Error"]
old-location: tapi3\itcallmediaevent_get_error.htm
tech.root: tapi3
ms.assetid: 6a6b84f1-700e-42e5-9127-161a6c078235
ms.date: 12/05/2018
ms.keywords: ITCallMediaEvent interface [TAPI 2.2],get_Error method, ITCallMediaEvent.get_Error, ITCallMediaEvent::get_Error, _tapi3_itcallmediaevent_get_error, get_Error, get_Error method [TAPI 2.2], get_Error method [TAPI 2.2],ITCallMediaEvent interface, tapi3.itcallmediaevent_get_error, tapi3if/ITCallMediaEvent::get_Error
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
 - ITCallMediaEvent::get_Error
 - tapi3if/ITCallMediaEvent::get_Error
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
 - ITCallMediaEvent.get_Error
---

# ITCallMediaEvent::get_Error


## -description

The 
<b>get_Error</b> method gets the error associated with the media event, if any.

## -parameters

### -param phrError [out]

Pointer to error.

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
The <i>phrError</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent">ITCallMediaEvent</a>