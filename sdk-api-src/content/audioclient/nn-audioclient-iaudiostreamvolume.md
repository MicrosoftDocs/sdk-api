---
UID: NN:audioclient.IAudioStreamVolume
title: IAudioStreamVolume (audioclient.h)
description: The IAudioStreamVolume interface enables a client to control and monitor the volume levels for all of the channels in an audio stream.helpviewer_keywords: ["IAudioStreamVolume","IAudioStreamVolume interface [Core Audio]","IAudioStreamVolume interface [Core Audio]","described","audioclient/IAudioStreamVolume","coreaudio.iaudiostreamvolume"]
old-location: coreaudio\iaudiostreamvolume.htm
tech.root: CoreAudio
ms.assetid: 92cc127b-77ac-4fc7-ac3c-319e5d6368d3
ms.date: 12/05/2018
ms.keywords: IAudioStreamVolume, IAudioStreamVolume interface [Core Audio], IAudioStreamVolume interface [Core Audio],described, audioclient/IAudioStreamVolume, coreaudio.iaudiostreamvolume
f1_keywords:
- audioclient/IAudioStreamVolume
dev_langs:
- c++
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Audioclient.h
api_name:
- IAudioStreamVolume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioStreamVolume interface


## -description



The <b>IAudioStreamVolume</b> interface enables a client to control and monitor the volume levels for all of the channels in an audio stream. The client obtains a reference to the <b>IAudioStreamVolume</b> interface on a stream object by calling the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioStreamVolume.

The effective volume level of any channel in the session submix, as heard at the speakers, is the product of the following four volume-level factors:

<ul>
<li>The per-channel volume levels of the streams in the session, which clients can control through the methods in the <b>IAudioStreamVolume</b> interface.</li>
<li>The per-channel volume level of the session, which clients can control through the methods in the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume</a> interface.</li>
<li>The master volume level of the session, which clients can control through the methods in the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume</a> interface.</li>
<li>The policy-based volume level of the session, which the system dynamically assigns to the session as the global mix changes.</li>
</ul>
Each of the four volume-level factors in the preceding list is a value in the range 0.0 to 1.0, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). The effective volume level is also a value in the range 0.0 to 1.0.

When releasing an <b>IAudioStreamVolume</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

The <b>IAudioStreamVolume</b> interface controls the channel volumes in a shared-mode audio stream. This interface does not work with exclusive-mode streams. For information about volume controls for exclusive-mode streams, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/endpointvolume-api">EndpointVolume API</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioStreamVolume</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioStreamVolume</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioStreamVolume</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-getallvolumes">GetAllVolumes</a>
</td>
<td align="left" width="63%">
Retrieves the volume levels for all the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-getchannelcount">GetChannelCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of channels contained in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-getchannelvolume">GetChannelVolume</a>
</td>
<td align="left" width="63%">
Retrieves the volume level for the specified channel in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-setallvolumes">SetAllVolumes</a>
</td>
<td align="left" width="63%">
Sets the individual volume levels for all the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-setchannelvolume">SetChannelVolume</a>
</td>
<td align="left" width="63%">
Sets the volume level for the specified channel in the audio stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a>
 

 

