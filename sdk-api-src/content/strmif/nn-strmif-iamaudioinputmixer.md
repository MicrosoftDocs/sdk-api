---
UID: NN:strmif.IAMAudioInputMixer
title: IAMAudioInputMixer
author: windows-sdk-content
description: The IAMAudioInputMixer interface controls audio capture properties, such as panning and loudness; and enables or disables specific audio inputs, such as the line in or the microphone.The Audio Capture filter exposes this interface on each input pin, as well as on the filter itself. The input pins on the Audio Capture Filter represent physical hardware connections; they are not connected to other DirectShow filters. The pin name indicates the input type; for example, &#0034;Line In&#0034; or &#0034;Microphone.&#0034; Use the IAMAudioInputMixer interface as follows:To control the settings on a particular input, use the interface on the pin.To set the overall properties when multiple inputs are enabled, use the interface on the filter.To enable or disable an input, call that pin's IAMAudioInputMixer::put_Enable method.Some methods on this interface might fail, depening on the capabilities of the underlying hardware.Filter Developers:\_Implement this interface on each input pin of an audio capture filter. You can also implement this interface on the audio capture filter itself to control the overall audio settings after mixing.
old-location: dshow\iamaudioinputmixer.htm
tech.root: DirectShow
ms.assetid: 217cb49d-7f5f-42c5-83db-546621f6a375
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAMAudioInputMixer, IAMAudioInputMixer interface [DirectShow], IAMAudioInputMixer interface [DirectShow],described, IAMAudioInputMixerInterface, dshow.iamaudioinputmixer, strmif/IAMAudioInputMixer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAudioInputMixer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAudioInputMixer interface


## -description



The <code>IAMAudioInputMixer</code> interface controls audio capture properties, such as panning and loudness; and enables or disables specific audio inputs, such as the line in or the microphone.

The <a href="https://msdn.microsoft.com/f76d5c82-33b2-4579-9420-8f97eca53ede">Audio Capture</a> filter exposes this interface on each input pin, as well as on the filter itself. The input pins on the Audio Capture Filter represent physical hardware connections; they are not connected to other DirectShow filters. The pin name indicates the input type; for example, "Line In" or "Microphone." Use the <code>IAMAudioInputMixer</code> interface as follows:

<ul>
<li>To control the settings on a particular input, use the interface on the pin.</li>
<li>To set the overall properties when multiple inputs are enabled, use the interface on the filter.</li>
<li>To enable or disable an input, call that pin's <a href="https://msdn.microsoft.com/84f179bf-2e2f-4ba0-81b7-c20acd09ccea">IAMAudioInputMixer::put_Enable</a> method.</li>
</ul>
Some methods on this interface might fail, depening on the capabilities of the underlying hardware.

<b>Filter Developers</b>: Implement this interface on each input pin of an audio capture filter. You can also implement this interface on the audio capture filter itself to control the overall audio settings after mixing.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMAudioInputMixer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMAudioInputMixer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMAudioInputMixer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08edf6be-81b7-4402-a500-1b7d9c389042">get_Bass</a>
</td>
<td align="left" width="63%">
Retrieves the bass equalization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0a77f8c-8608-4e16-bc7a-3c90dde2aad8">get_BassRange</a>
</td>
<td align="left" width="63%">
Retrieves the bass range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3ec509c-9990-4803-a4e3-abc88fc8c522">get_Enable</a>
</td>
<td align="left" width="63%">
Queries whether an input is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/620003c0-401f-4415-a82f-a80e7b32dbd3">get_Loudness</a>
</td>
<td align="left" width="63%">
Retrieves the loudness control setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdf8f90b-72a4-4faf-9d08-2634582245f8">get_MixLevel</a>
</td>
<td align="left" width="63%">
Retrieves the recording level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c0ce59d-6083-4af2-856b-41a1c9d83295">get_Mono</a>
</td>
<td align="left" width="63%">
Queries whether all the channels of an input are combined into a mono signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa1aae16-484e-4f78-901e-2fdb0d8e365c">get_Pan</a>
</td>
<td align="left" width="63%">
Retrieves the pan level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6876e121-cb04-49f9-aee4-27759f93529b">get_Treble</a>
</td>
<td align="left" width="63%">
Retrieves the treble equalization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/726cbdda-5772-43bc-846f-f7d1672cc56f">get_TrebleRange</a>
</td>
<td align="left" width="63%">
Retrieves the treble range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf752767-826d-487d-ae05-9737765975c8">put_Bass</a>
</td>
<td align="left" width="63%">
Sets the bass equalization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84f179bf-2e2f-4ba0-81b7-c20acd09ccea">put_Enable</a>
</td>
<td align="left" width="63%">
Enables or disables an input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4baca46-260c-45fe-8c03-304c906aab15">put_Loudness</a>
</td>
<td align="left" width="63%">
Sets the loudness control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07fd327f-d78b-4fc0-9c6a-69cdaa2bcdf6">put_MixLevel</a>
</td>
<td align="left" width="63%">
Sets the recording level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb45a1ad-b6d8-4129-97f3-a9c99053c0f0">put_Mono</a>
</td>
<td align="left" width="63%">
Combines all channels of an input into a mono signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb0528e0-81d0-45a3-831a-8cf3ff1232b6">put_Pan</a>
</td>
<td align="left" width="63%">
Sets the pan level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09030c17-14d0-4af2-9e9e-64a536133b64">put_Treble</a>
</td>
<td align="left" width="63%">
Sets the treble equalization.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

