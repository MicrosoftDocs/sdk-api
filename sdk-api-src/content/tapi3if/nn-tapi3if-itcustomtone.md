---
UID: NN:tapi3if.ITCustomTone
title: ITCustomTone
author: windows-driver-content
description: The ITCustomTone interface exposes methods that allow detailed control over the custom tones that are available with some phone sets.
old-location: tapi3\itcustomtone.htm
old-project: Tapi
ms.assetid: f2c51048-93aa-4469-b00e-911e62b5702d
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITCustomTone, ITCustomTone interface [TAPI 2.2], ITCustomTone interface [TAPI 2.2],described, _tapi3_itcustomtone, tapi3.itcustomtone, tapi3if/ITCustomTone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITCustomTone
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCustomTone interface


## -description


The 
<b>ITCustomTone</b> interface exposes methods that allow detailed control over the custom tones that are available with some phone sets. The 
<a href="https://msdn.microsoft.com/addef387-9d92-4da3-af4c-b4d40bde2e36">ITLegacyCallMediaControl2::CreateCustomToneObject</a> and 
<a href="https://msdn.microsoft.com/5115192e-68de-4779-92dc-7cf63585faae">ITLegacyCallMediaControl2::GenerateCustomTonesByCollection</a> methods create the 
<b>ITCustomTone</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCustomTone</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITCustomTone</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0d561ab6-fc38-4058-9443-d7825eae2dc5">get_CadenceOff</a>
</td>
<td align="left" width="63%">
Gets the "off" duration, in milliseconds, of the cadence of the custom tone to generate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f3da359-69e1-40a3-bfd6-42ade8de2379">get_CadenceOn</a>
</td>
<td align="left" width="63%">
Gets the "on" duration, in milliseconds, of the cadence of the custom tone to generate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2521d754-234a-4ef0-a3b2-23cea999ad45">get_Frequency</a>
</td>
<td align="left" width="63%">
Gets the frequency, in hertz, of the tone component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28eead55-915a-4bb6-9915-ebd56c9d123d">get_Volume</a>
</td>
<td align="left" width="63%">
Gets the volume level at which to generate the tone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/056e1ca5-2bce-4a69-9b30-2ac142bcb52b">put_CadenceOff</a>
</td>
<td align="left" width="63%">
Sets the "off" duration, in milliseconds, of the cadence of the custom tone to generate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4403c3a-7dd8-4707-ac23-5a478fffce17">put_CadenceOn</a>
</td>
<td align="left" width="63%">
Sets the "on" duration, in milliseconds, of the cadence of the custom tone to generate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1faae20a-40a7-48d7-9621-5f1761c28773">put_Frequency</a>
</td>
<td align="left" width="63%">
Sets the frequency, in hertz, of the tone component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2de6dbc3-9a3d-48e7-b9e1-56b3e25d1b60">put_Volume</a>
</td>
<td align="left" width="63%">
Sets the volume level at which to generate the tone.

</td>
</tr>
</table> 

