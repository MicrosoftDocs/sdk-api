---
UID: NN:strmif.IAMAudioInputMixer
title: IAMAudioInputMixer (strmif.h)
author: windows-sdk-content
description: The IAMAudioInputMixer interface controls audio capture properties, such as panning and loudness; and enables or disables specific audio inputs, such as the line in or the microphone.The Audio Capture filter exposes this interface on each input pin, as well as on the filter itself. The input pins on the Audio Capture Filter represent physical hardware connections; they are not connected to other DirectShow filters. The pin name indicates the input type; for example, &#0034;Line In&#0034; or &#0034;Microphone.&#0034; Use the IAMAudioInputMixer interface as follows:To control the settings on a particular input, use the interface on the pin.To set the overall properties when multiple inputs are enabled, use the interface on the filter.To enable or disable an input, call that pin's IAMAudioInputMixer::put_Enable method.Some methods on this interface might fail, depening on the capabilities of the underlying hardware.Filter Developers:\_Implement this interface on each input pin of an audio capture filter. You can also implement this interface on the audio capture filter itself to control the overall audio settings after mixing.
old-location: dshow\iamaudioinputmixer.htm
tech.root: DirectShow
ms.assetid: 217cb49d-7f5f-42c5-83db-546621f6a375
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMAudioInputMixer, IAMAudioInputMixer interface [DirectShow], IAMAudioInputMixer interface [DirectShow],described, IAMAudioInputMixerInterface, dshow.iamaudioinputmixer, strmif/IAMAudioInputMixer
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
ms.custom: 19H1
---

# IAMAudioInputMixer interface


## -description



The <code>IAMAudioInputMixer</code> interface controls audio capture properties, such as panning and loudness; and enables or disables specific audio inputs, such as the line in or the microphone.

The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/audio-capture-filter">Audio Capture</a> filter exposes this interface on each input pin, as well as on the filter itself. The input pins on the Audio Capture Filter represent physical hardware connections; they are not connected to other DirectShow filters. The pin name indicates the input type; for example, "Line In" or "Microphone." Use the <code>IAMAudioInputMixer</code> interface as follows:

<ul>
<li>To control the settings on a particular input, use the interface on the pin.</li>
<li>To set the overall properties when multiple inputs are enabled, use the interface on the filter.</li>
<li>To enable or disable an input, call that pin's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_enable">IAMAudioInputMixer::put_Enable</a> method.</li>
</ul>
Some methods on this interface might fail, depening on the capabilities of the underlying hardware.

<b>Filter Developers</b>: Implement this interface on each input pin of an audio capture filter. You can also implement this interface on the audio capture filter itself to control the overall audio settings after mixing.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMAudioInputMixer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMAudioInputMixer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_bass">get_Bass</a>
</td>
<td align="left" width="63%">
Retrieves the bass equalization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_bassrange">get_BassRange</a>
</td>
<td align="left" width="63%">
Retrieves the bass range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_enable">get_Enable</a>
</td>
<td align="left" width="63%">
Queries whether an input is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_loudness">get_Loudness</a>
</td>
<td align="left" width="63%">
Retrieves the loudness control setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_mixlevel">get_MixLevel</a>
</td>
<td align="left" width="63%">
Retrieves the recording level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_mono">get_Mono</a>
</td>
<td align="left" width="63%">
Queries whether all the channels of an input are combined into a mono signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_pan">get_Pan</a>
</td>
<td align="left" width="63%">
Retrieves the pan level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_treble">get_Treble</a>
</td>
<td align="left" width="63%">
Retrieves the treble equalization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_treblerange">get_TrebleRange</a>
</td>
<td align="left" width="63%">
Retrieves the treble range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_bass">put_Bass</a>
</td>
<td align="left" width="63%">
Sets the bass equalization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_enable">put_Enable</a>
</td>
<td align="left" width="63%">
Enables or disables an input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_loudness">put_Loudness</a>
</td>
<td align="left" width="63%">
Sets the loudness control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_mixlevel">put_MixLevel</a>
</td>
<td align="left" width="63%">
Sets the recording level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_mono">put_Mono</a>
</td>
<td align="left" width="63%">
Combines all channels of an input into a mono signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_pan">put_Pan</a>
</td>
<td align="left" width="63%">
Sets the pan level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_treble">put_Treble</a>
</td>
<td align="left" width="63%">
Sets the treble equalization.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

