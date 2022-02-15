---
UID: NN:xaudio2.IXAudio2Voice
title: IXAudio2Voice (xaudio2.h)
description: IXAudio2Voice represents the base interface from which IXAudio2SourceVoice, IXAudio2SubmixVoice and IXAudio2MasteringVoice are derived. The methods listed below are common to all voice subclasses.
helpviewer_keywords: ["IXAudio2Voice","IXAudio2Voice Interface","IXAudio2Voice Interface interface [XAudio2 Audio Mixing APIs]","IXAudio2Voice Interface interface [XAudio2 Audio Mixing APIs]","described","xaudio2.ixaudio2voice","xaudio2/IXAudio2Voice"]
old-location: xaudio2\ixaudio2voice.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice
ms.date: 12/05/2018
ms.keywords: IXAudio2Voice, IXAudio2Voice Interface, IXAudio2Voice Interface interface [XAudio2 Audio Mixing APIs], IXAudio2Voice Interface interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2voice, xaudio2/IXAudio2Voice
req.header: xaudio2.h
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2Voice
 - xaudio2/IXAudio2Voice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - IXAudio2Voice Interface
---

# IXAudio2Voice interface


## -description

<b>IXAudio2Voice</b> represents the base interface from which <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice">IXAudio2SubmixVoice</a> and <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice">IXAudio2MasteringVoice</a> are derived. The methods listed below are common to all voice subclasses.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice">DestroyVoice</a>
</td>
<td align="left" width="63%">
Destroys the voice. If necessary, stops the voice and removes it from the XAudio2 graph.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect">DisableEffect</a>
</td>
<td align="left" width="63%">
Disables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect">EnableEffect</a>
</td>
<td align="left" width="63%">
Enables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-getchannelvolumes">GetChannelVolumes</a>
</td>
<td align="left" width="63%">
Returns the volume levels for the voice, per channel.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-geteffectparameters">GetEffectParameters</a>
</td>
<td align="left" width="63%">
Returns the current effect-specific parameters of a given effect in the voice's effect chain.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-geteffectstate">GetEffectState</a>
</td>
<td align="left" width="63%">
Returns the running state of the effect at a specified position in the effect chain of the voice.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-getfilterparameters">GetFilterParameters</a>
</td>
<td align="left" width="63%">
Gets the voice's filter parameters.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-getoutputfilterparameters">GetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Returns the filter parameters from one of this voice's sends.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-getoutputmatrix">GetOutputMatrix</a>
</td>
<td align="left" width="63%">
Gets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails">GetVoiceDetails</a>
</td>
<td align="left" width="63%">
Returns information about the creation flags, input channels, and sample rate of a voice.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-getvolume">GetVolume</a>
</td>
<td align="left" width="63%">
Gets the current overall volume level of the voice.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes">SetChannelVolumes</a>
</td>
<td align="left" width="63%">
Sets the volume levels for the voice, per channel.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain">SetEffectChain</a>
</td>
<td align="left" width="63%">
Replaces the effect chain of the voice.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters">SetEffectParameters</a>
</td>
<td align="left" width="63%">
Sets parameters for a given effect in the voice's effect chain.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters">SetFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the voice's filter parameters.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters">SetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the filter parameters on one of this voice's sends.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix">SetOutputMatrix</a>
</td>
<td align="left" width="63%">
Sets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices">SetOutputVoices</a>
</td>
<td align="left" width="63%">
Designates a new set of submix or mastering voices to receive the output of the voice.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume">SetVolume</a>
</td>
<td align="left" width="63%">
Sets the overall volume level for the voice.

</td>
</tr>
</table>

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/interfaces">XAudio2 Interfaces</a>
