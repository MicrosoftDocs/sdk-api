---
UID: NN:tapi3if.ITCustomTone
title: ITCustomTone (tapi3if.h)
description: The ITCustomTone interface exposes methods that allow detailed control over the custom tones that are available with some phone sets.
helpviewer_keywords: ["ITCustomTone","ITCustomTone interface [TAPI 2.2]","ITCustomTone interface [TAPI 2.2]","described","_tapi3_itcustomtone","tapi3.itcustomtone","tapi3if/ITCustomTone"]
old-location: tapi3\itcustomtone.htm
tech.root: tapi3
ms.assetid: f2c51048-93aa-4469-b00e-911e62b5702d
ms.date: 12/05/2018
ms.keywords: ITCustomTone, ITCustomTone interface [TAPI 2.2], ITCustomTone interface [TAPI 2.2],described, _tapi3_itcustomtone, tapi3.itcustomtone, tapi3if/ITCustomTone
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
 - ITCustomTone
 - tapi3if/ITCustomTone
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
 - ITCustomTone
---

# ITCustomTone interface


## -description

The 
<b>ITCustomTone</b> interface exposes methods that allow detailed control over the custom tones that are available with some phone sets. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-createcustomtoneobject">ITLegacyCallMediaControl2::CreateCustomToneObject</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtonesbycollection">ITLegacyCallMediaControl2::GenerateCustomTonesByCollection</a> methods create the 
<b>ITCustomTone</b> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCustomTone</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCustomTone</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCustomTone</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-get_cadenceoff">get_CadenceOff</a>
</td>
<td align="left" width="63%">
Gets the "off" duration, in milliseconds, of the cadence of the custom tone to generate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-get_cadenceon">get_CadenceOn</a>
</td>
<td align="left" width="63%">
Gets the "on" duration, in milliseconds, of the cadence of the custom tone to generate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-get_frequency">get_Frequency</a>
</td>
<td align="left" width="63%">
Gets the frequency, in hertz, of the tone component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-get_volume">get_Volume</a>
</td>
<td align="left" width="63%">
Gets the volume level at which to generate the tone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-put_cadenceoff">put_CadenceOff</a>
</td>
<td align="left" width="63%">
Sets the "off" duration, in milliseconds, of the cadence of the custom tone to generate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-put_cadenceon">put_CadenceOn</a>
</td>
<td align="left" width="63%">
Sets the "on" duration, in milliseconds, of the cadence of the custom tone to generate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-put_frequency">put_Frequency</a>
</td>
<td align="left" width="63%">
Sets the frequency, in hertz, of the tone component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-put_volume">put_Volume</a>
</td>
<td align="left" width="63%">
Sets the volume level at which to generate the tone.

</td>
</tr>
</table>