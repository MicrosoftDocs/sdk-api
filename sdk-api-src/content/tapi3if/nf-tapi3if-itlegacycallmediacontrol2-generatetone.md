---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GenerateTone
title: ITLegacyCallMediaControl2::GenerateTone (tapi3if.h)
description: The GenerateTone method generates the specified tone.
helpviewer_keywords: ["GenerateTone","GenerateTone method [TAPI 2.2]","GenerateTone method [TAPI 2.2]","ITLegacyCallMediaControl2 interface","ITLegacyCallMediaControl2 interface [TAPI 2.2]","GenerateTone method","ITLegacyCallMediaControl2.GenerateTone","ITLegacyCallMediaControl2::GenerateTone","_tapi3_itlegacycallmediacontrol2_generatetone","tapi3.itlegacycallmediacontrol2_generatetone","tapi3if/ITLegacyCallMediaControl2::GenerateTone"]
old-location: tapi3\itlegacycallmediacontrol2_generatetone.htm
tech.root: tapi3
ms.assetid: 4c77ee53-3c40-4fdc-9a35-40a8e74b4ec4
ms.date: 12/05/2018
ms.keywords: GenerateTone, GenerateTone method [TAPI 2.2], GenerateTone method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GenerateTone method, ITLegacyCallMediaControl2.GenerateTone, ITLegacyCallMediaControl2::GenerateTone, _tapi3_itlegacycallmediacontrol2_generatetone, tapi3.itlegacycallmediacontrol2_generatetone, tapi3if/ITLegacyCallMediaControl2::GenerateTone
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
 - ITLegacyCallMediaControl2::GenerateTone
 - tapi3if/ITLegacyCallMediaControl2::GenerateTone
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
 - ITLegacyCallMediaControl2.GenerateTone
---

# ITLegacyCallMediaControl2::GenerateTone


## -description

The 
<b>GenerateTone</b> method generates the specified tone.

To generate custom tones, call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtones">GenerateCustomTones</a> (C/C++) or the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtonesbycollection">GenerateCustomTonesByCollection</a> method (Visual Basic and scripting applications).

## -parameters

### -param ToneMode [in]

Indicates the tone mode. The values used are those from the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_tonemode">TAPI_TONEMODE</a> enumeration.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

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
<a href="/windows/desktop/api/tapi/nf-tapi-linegeneratetone">lineGenerateTone</a> function.

When tone generation finishes, an event of type TE_GENERATEEVENT is generated.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>