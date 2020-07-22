---
UID: NN:mfidl.IMFAudioStreamVolume
title: IMFAudioStreamVolume (mfidl.h)
description: Controls the volume levels of individual audio channels.
helpviewer_keywords: ["IMFAudioStreamVolume","IMFAudioStreamVolume interface [Media Foundation]","IMFAudioStreamVolume interface [Media Foundation]","described","f06ed262-a2ec-4688-b477-877d04cf1892","mf.imfaudiostreamvolume","mfidl/IMFAudioStreamVolume"]
old-location: mf\imfaudiostreamvolume.htm
tech.root: mf
ms.assetid: f06ed262-a2ec-4688-b477-877d04cf1892
ms.date: 12/05/2018
ms.keywords: IMFAudioStreamVolume, IMFAudioStreamVolume interface [Media Foundation], IMFAudioStreamVolume interface [Media Foundation],described, f06ed262-a2ec-4688-b477-877d04cf1892, mf.imfaudiostreamvolume, mfidl/IMFAudioStreamVolume
f1_keywords:
- mfidl/IMFAudioStreamVolume
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFAudioStreamVolume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFAudioStreamVolume interface


## -description


Controls the volume levels of individual audio channels.

The streaming audio renderer (SAR) exposes this interface as a service. To get a pointer to the interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier <b>MR_STREAM_VOLUME_SERVICE</b>. You can call <b>GetService</b> directly on the SAR or call it on the Media Session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAudioStreamVolume</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFAudioStreamVolume</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFAudioStreamVolume</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiostreamvolume-getallvolumes">GetAllVolumes</a>
</td>
<td align="left" width="63%">
Retrieves the volume levels for all of the channels in the audio stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiostreamvolume-getchannelcount">GetChannelCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of channels in the audio stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiostreamvolume-getchannelvolume">GetChannelVolume</a>
</td>
<td align="left" width="63%">
Retrieves the volume level for a specified channel in the audio stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiostreamvolume-setallvolumes">SetAllVolumes</a>
</td>
<td align="left" width="63%">
Sets the individual volume levels for all of the channels in the audio stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiostreamvolume-setchannelvolume">SetChannelVolume</a>
</td>
<td align="left" width="63%">
Sets the volume level for a specified channel in the audio stream.
        

</td>
</tr>
</table> 


## -remarks



If your application does not require channel-level volume control, you can use the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume">IMFSimpleAudioVolume</a> interface to control the master volume level of the audio session.

Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). For each channel, the attenuation level is the product of:

<ul>
<li>The master volume level of the audio session.
          </li>
<li>The volume level of the channel.
          </li>
</ul>
For example, if the master volume is 0.8 and the channel volume is 0.5, the attenuation for that channel is 0.8 × 0.5 = 0.4. Volume levels can exceed 1.0 (positive gain), but the audio engine clips any audio samples that exceed zero decibels.

Use the following formula to convert the volume level to the decibel (dB) scale:

Attenuation (dB) = 20 * log10(<i>Level</i>)

For example, a volume level of 0.50 represents 6.02 dB of attenuation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>
 

 

