---
UID: NF:tapi3if.ITLegacyCallMediaControl.GenerateDigits
title: ITLegacyCallMediaControl::GenerateDigits (tapi3if.h)
description: The GenerateDigits method causes digits to be output on the current call.
helpviewer_keywords: ["GenerateDigits","GenerateDigits method [TAPI 2.2]","GenerateDigits method [TAPI 2.2]","ITLegacyCallMediaControl interface","ITLegacyCallMediaControl interface [TAPI 2.2]","GenerateDigits method","ITLegacyCallMediaControl.GenerateDigits","ITLegacyCallMediaControl::GenerateDigits","_tapi3_itlegacycallmediacontrol_generatedigits","tapi3.itlegacycallmediacontrol_generatedigits","tapi3if/ITLegacyCallMediaControl::GenerateDigits"]
old-location: tapi3\itlegacycallmediacontrol_generatedigits.htm
tech.root: tapi3
ms.assetid: d4dcdce0-4df5-43bb-a5ea-ea72782d5f04
ms.date: 12/05/2018
ms.keywords: GenerateDigits, GenerateDigits method [TAPI 2.2], GenerateDigits method [TAPI 2.2],ITLegacyCallMediaControl interface, ITLegacyCallMediaControl interface [TAPI 2.2],GenerateDigits method, ITLegacyCallMediaControl.GenerateDigits, ITLegacyCallMediaControl::GenerateDigits, _tapi3_itlegacycallmediacontrol_generatedigits, tapi3.itlegacycallmediacontrol_generatedigits, tapi3if/ITLegacyCallMediaControl::GenerateDigits
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
 - ITLegacyCallMediaControl::GenerateDigits
 - tapi3if/ITLegacyCallMediaControl::GenerateDigits
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
 - ITLegacyCallMediaControl.GenerateDigits
---

# ITLegacyCallMediaControl::GenerateDigits


## -description

The 
<b>GenerateDigits</b> method causes digits to be output on the current call.

## -parameters

### -param pDigits [in]

Pointer to <b>BSTR</b> representation of digits to be sent.

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

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDigits</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol">ITLegacyCallMediaControl</a>