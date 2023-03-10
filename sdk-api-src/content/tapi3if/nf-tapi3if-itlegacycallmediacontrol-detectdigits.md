---
UID: NF:tapi3if.ITLegacyCallMediaControl.DetectDigits
title: ITLegacyCallMediaControl::DetectDigits (tapi3if.h)
description: The DetectDigits method sets an identifier of the type of digits that will be detected on the current call, such as rotary pulse or DTMF.
helpviewer_keywords: ["DetectDigits","DetectDigits method [TAPI 2.2]","DetectDigits method [TAPI 2.2]","ITLegacyCallMediaControl interface","ITLegacyCallMediaControl interface [TAPI 2.2]","DetectDigits method","ITLegacyCallMediaControl.DetectDigits","ITLegacyCallMediaControl::DetectDigits","_tapi3_itlegacycallmediacontrol_detectdigits","tapi3.itlegacycallmediacontrol_detectdigits","tapi3if/ITLegacyCallMediaControl::DetectDigits"]
old-location: tapi3\itlegacycallmediacontrol_detectdigits.htm
tech.root: tapi3
ms.assetid: 09adb3fb-cf77-4c8b-beab-85d173cbb242
ms.date: 12/05/2018
ms.keywords: DetectDigits, DetectDigits method [TAPI 2.2], DetectDigits method [TAPI 2.2],ITLegacyCallMediaControl interface, ITLegacyCallMediaControl interface [TAPI 2.2],DetectDigits method, ITLegacyCallMediaControl.DetectDigits, ITLegacyCallMediaControl::DetectDigits, _tapi3_itlegacycallmediacontrol_detectdigits, tapi3.itlegacycallmediacontrol_detectdigits, tapi3if/ITLegacyCallMediaControl::DetectDigits
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
 - ITLegacyCallMediaControl::DetectDigits
 - tapi3if/ITLegacyCallMediaControl::DetectDigits
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
 - ITLegacyCallMediaControl.DetectDigits
---

# ITLegacyCallMediaControl::DetectDigits


## -description

The 
<b>DetectDigits</b> method sets an identifier of the type of digits that will be detected on the current call, such as rotary pulse or DTMF.

## -parameters

### -param DigitMode [in]

Indicates 
<a href="/windows/desktop/Tapi/tapi-digitmode--constants">digit mode</a>.

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
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
No call currently exists.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol">ITLegacyCallMediaControl</a>