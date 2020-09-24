---
UID: NF:tapi3if.ITCallingCard.get_NumberOfDigits
title: ITCallingCard::get_NumberOfDigits (tapi3if.h)
description: The get_NumberOfDigits method gets the number of digits in the existing card number.
helpviewer_keywords: ["ITCallingCard interface [TAPI 2.2]","get_NumberOfDigits method","ITCallingCard.get_NumberOfDigits","ITCallingCard::get_NumberOfDigits","_tapi3_itcallingcard_get_numberofdigits","get_NumberOfDigits","get_NumberOfDigits method [TAPI 2.2]","get_NumberOfDigits method [TAPI 2.2]","ITCallingCard interface","tapi3.itcallingcard_get_numberofdigits","tapi3if/ITCallingCard::get_NumberOfDigits"]
old-location: tapi3\itcallingcard_get_numberofdigits.htm
tech.root: tapi3
ms.assetid: 9eacfd2d-b137-4923-9cfa-139473ba8298
ms.date: 12/05/2018
ms.keywords: ITCallingCard interface [TAPI 2.2],get_NumberOfDigits method, ITCallingCard.get_NumberOfDigits, ITCallingCard::get_NumberOfDigits, _tapi3_itcallingcard_get_numberofdigits, get_NumberOfDigits, get_NumberOfDigits method [TAPI 2.2], get_NumberOfDigits method [TAPI 2.2],ITCallingCard interface, tapi3.itcallingcard_get_numberofdigits, tapi3if/ITCallingCard::get_NumberOfDigits
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
 - ITCallingCard::get_NumberOfDigits
 - tapi3if/ITCallingCard::get_NumberOfDigits
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
 - ITCallingCard.get_NumberOfDigits
---

# ITCallingCard::get_NumberOfDigits


## -description

The 
<b>get_NumberOfDigits</b> method gets the number of digits in the existing card number.

## -parameters

### -param plDigits [out]

Pointer to number of digits in the card number.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>plDigits</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plDigits</i> parameter is not a valid pointer.

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

The card number itself is not returned for security reasons. The application can use this information to insert filler bytes into a text control in "password" mode to show that a number exists.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard">ITCallingCard</a>