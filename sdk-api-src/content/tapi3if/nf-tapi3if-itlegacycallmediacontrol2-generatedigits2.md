---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GenerateDigits2
title: ITLegacyCallMediaControl2::GenerateDigits2 (tapi3if.h)
description: The GenerateDigits2 method causes digits to be output on the current call. This method extends the ITLegacyCallMediaControl::GenerateDigits method by adding a duration parameter.
helpviewer_keywords: ["GenerateDigits2","GenerateDigits2 method [TAPI 2.2]","GenerateDigits2 method [TAPI 2.2]","ITLegacyCallMediaControl2 interface","ITLegacyCallMediaControl2 interface [TAPI 2.2]","GenerateDigits2 method","ITLegacyCallMediaControl2.GenerateDigits2","ITLegacyCallMediaControl2::GenerateDigits2","_tapi3_itlegacycallmediacontrol2_generatedigits2","tapi3.itlegacycallmediacontrol2_generatedigits2","tapi3if/ITLegacyCallMediaControl2::GenerateDigits2"]
old-location: tapi3\itlegacycallmediacontrol2_generatedigits2.htm
tech.root: tapi3
ms.assetid: 63ea18ef-18ca-4771-a7d9-60d4e8c514a5
ms.date: 12/05/2018
ms.keywords: GenerateDigits2, GenerateDigits2 method [TAPI 2.2], GenerateDigits2 method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GenerateDigits2 method, ITLegacyCallMediaControl2.GenerateDigits2, ITLegacyCallMediaControl2::GenerateDigits2, _tapi3_itlegacycallmediacontrol2_generatedigits2, tapi3.itlegacycallmediacontrol2_generatedigits2, tapi3if/ITLegacyCallMediaControl2::GenerateDigits2
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
 - ITLegacyCallMediaControl2::GenerateDigits2
 - tapi3if/ITLegacyCallMediaControl2::GenerateDigits2
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
 - ITLegacyCallMediaControl2.GenerateDigits2
---

# ITLegacyCallMediaControl2::GenerateDigits2


## -description

The 
<b>GenerateDigits2</b> method causes digits to be output on the current call. This method extends the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-generatedigits">ITLegacyCallMediaControl::GenerateDigits</a> method by adding a duration parameter.

## -parameters

### -param pDigits [in]

A pointer to a <b>BSTR</b> representation of the digits to generate.

### -param DigitMode [in]

Indicates the digit mode. Valid values are those from the TAPI 2.<i>x</i>
<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_constants</a>.

### -param lDuration [in]

Both the duration, in milliseconds, of DTMF digits and pulse, and DTMF interdigit spacing.

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
The <i>pDigits</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The call must be in the <i>connected</i> state.

</td>
</tr>
</table>

## -remarks

This method translates to a call to the TAPI 2.<i>x</i>
<a href="/windows/desktop/api/tapi/nf-tapi-linegeneratedigits">lineGenerateDigits</a> function.

When digit generation finishes, an event of type TE_GENERATEEVENT is generated.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>