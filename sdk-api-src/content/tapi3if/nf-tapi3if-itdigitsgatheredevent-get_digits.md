---
UID: NF:tapi3if.ITDigitsGatheredEvent.get_Digits
title: ITDigitsGatheredEvent::get_Digits (tapi3if.h)
description: The get_Digits method gets the gathered digits for the call.
helpviewer_keywords: ["ITDigitsGatheredEvent interface [TAPI 2.2]","get_Digits method","ITDigitsGatheredEvent.get_Digits","ITDigitsGatheredEvent::get_Digits","_tapi3_itdigitsgatheredevent_get_digits","get_Digits","get_Digits method [TAPI 2.2]","get_Digits method [TAPI 2.2]","ITDigitsGatheredEvent interface","tapi3.itdigitsgatheredevent_get_digits","tapi3if/ITDigitsGatheredEvent::get_Digits"]
old-location: tapi3\itdigitsgatheredevent_get_digits.htm
tech.root: tapi3
ms.assetid: 940e186b-33bd-4846-8314-39ede19bad95
ms.date: 12/05/2018
ms.keywords: ITDigitsGatheredEvent interface [TAPI 2.2],get_Digits method, ITDigitsGatheredEvent.get_Digits, ITDigitsGatheredEvent::get_Digits, _tapi3_itdigitsgatheredevent_get_digits, get_Digits, get_Digits method [TAPI 2.2], get_Digits method [TAPI 2.2],ITDigitsGatheredEvent interface, tapi3.itdigitsgatheredevent_get_digits, tapi3if/ITDigitsGatheredEvent::get_Digits
req.header: tapi3if.h
req.include-header: 
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
 - ITDigitsGatheredEvent::get_Digits
 - tapi3if/ITDigitsGatheredEvent::get_Digits
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
 - ITDigitsGatheredEvent.get_Digits
---

# ITDigitsGatheredEvent::get_Digits


## -description

The 
<b>get_Digits</b> method gets the gathered digits for the call.

## -parameters

### -param ppDigits [out]

Pointer to a <b>BSTR</b> where the gathered digits are stored.

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
The <i>ppDigits</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitsgatheredevent">ITDigitsGatheredEvent</a>