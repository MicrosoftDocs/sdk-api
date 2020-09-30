---
UID: NF:tapi3if.ITDigitGenerationEvent.get_Call
title: ITDigitGenerationEvent::get_Call (tapi3if.h)
description: The get_Call method returns an ITCallInfo interface pointer for the call on which the event is required.
helpviewer_keywords: ["ITDigitGenerationEvent interface [TAPI 2.2]","get_Call method","ITDigitGenerationEvent.get_Call","ITDigitGenerationEvent::get_Call","_tapi3_itdigitgenerationevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITDigitGenerationEvent interface","tapi3.itdigitgenerationevent_get_call","tapi3if/ITDigitGenerationEvent::get_Call"]
old-location: tapi3\itdigitgenerationevent_get_call.htm
tech.root: tapi3
ms.assetid: b0f4281f-e1df-4be9-acfc-5482044eb44b
ms.date: 12/05/2018
ms.keywords: ITDigitGenerationEvent interface [TAPI 2.2],get_Call method, ITDigitGenerationEvent.get_Call, ITDigitGenerationEvent::get_Call, _tapi3_itdigitgenerationevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITDigitGenerationEvent interface, tapi3.itdigitgenerationevent_get_call, tapi3if/ITDigitGenerationEvent::get_Call
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
 - ITDigitGenerationEvent::get_Call
 - tapi3if/ITDigitGenerationEvent::get_Call
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
 - ITDigitGenerationEvent.get_Call
---

# ITDigitGenerationEvent::get_Call


## -description

The 
<b>get_Call</b> method returns an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface pointer for the call on which the event is required.

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

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitgenerationevent">ITDigitGenerationEvent</a>