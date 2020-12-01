---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GenerateCustomTonesByCollection
title: ITLegacyCallMediaControl2::GenerateCustomTonesByCollection (tapi3if.h)
description: The GenerateCustomTonesByCollection method generates the specified custom tone.
helpviewer_keywords: ["GenerateCustomTonesByCollection","GenerateCustomTonesByCollection method [TAPI 2.2]","GenerateCustomTonesByCollection method [TAPI 2.2]","ITLegacyCallMediaControl2 interface","ITLegacyCallMediaControl2 interface [TAPI 2.2]","GenerateCustomTonesByCollection method","ITLegacyCallMediaControl2.GenerateCustomTonesByCollection","ITLegacyCallMediaControl2::GenerateCustomTonesByCollection","_tapi3_itlegacycallmediacontrol2_generatecustomtonesbycollection","tapi3.itlegacycallmediacontrol2_generatecustomtonesbycollection","tapi3if/ITLegacyCallMediaControl2::GenerateCustomTonesByCollection"]
old-location: tapi3\itlegacycallmediacontrol2_generatecustomtonesbycollection.htm
tech.root: tapi3
ms.assetid: 5115192e-68de-4779-92dc-7cf63585faae
ms.date: 12/05/2018
ms.keywords: GenerateCustomTonesByCollection, GenerateCustomTonesByCollection method [TAPI 2.2], GenerateCustomTonesByCollection method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GenerateCustomTonesByCollection method, ITLegacyCallMediaControl2.GenerateCustomTonesByCollection, ITLegacyCallMediaControl2::GenerateCustomTonesByCollection, _tapi3_itlegacycallmediacontrol2_generatecustomtonesbycollection, tapi3.itlegacycallmediacontrol2_generatecustomtonesbycollection, tapi3if/ITLegacyCallMediaControl2::GenerateCustomTonesByCollection
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
 - ITLegacyCallMediaControl2::GenerateCustomTonesByCollection
 - tapi3if/ITLegacyCallMediaControl2::GenerateCustomTonesByCollection
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
 - ITLegacyCallMediaControl2.GenerateCustomTonesByCollection
---

# ITLegacyCallMediaControl2::GenerateCustomTonesByCollection


## -description

The 
<b>GenerateCustomTonesByCollection</b> method generates the specified custom tone.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtones">GenerateCustomTones</a> method instead.

## -parameters

### -param pCustomToneCollection [in]

Pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection2">ITCollection2</a> interface containing a collection of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcustomtone">ITCustomTone</a> interface pointers representing the tone's components. If the collection is a multifrequency tone, the various tones are played simultaneously.

### -param lDuration [in]

The duration, in milliseconds, during which the tone should be sustained. A value of zero uses a default duration.

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
The <i>pCustomToneCollection</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the tones buffer.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection2">ITCollection2</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcustomtone">ITCustomTone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>