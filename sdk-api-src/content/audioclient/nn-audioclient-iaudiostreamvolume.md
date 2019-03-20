---
UID: NN:audioclient.IAudioStreamVolume
title: IAudioStreamVolume (audioclient.h)
author: windows-sdk-content
description: The IAudioStreamVolume interface enables a client to control and monitor the volume levels for all of the channels in an audio stream.
old-location: coreaudio\iaudiostreamvolume.htm
tech.root: CoreAudio
ms.assetid: 92cc127b-77ac-4fc7-ac3c-319e5d6368d3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioStreamVolume, IAudioStreamVolume interface [Core Audio], IAudioStreamVolume interface [Core Audio],described, audioclient/IAudioStreamVolume, coreaudio.iaudiostreamvolume
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioStreamVolume interface


## -description



The <b>IAudioStreamVolume</b> interface enables a client to control and monitor the volume levels for all of the channels in an audio stream. The client obtains a reference to the <b>IAudioStreamVolume</b> interface on a stream object by calling the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioStreamVolume.

The effective volume level of any channel in the session submix, as heard at the speakers, is the product of the following four volume-level factors:

<ul>
<li>The per-channel volume levels of the streams in the session, which clients can control through the methods in the <b>IAudioStreamVolume</b> interface.</li>
<li>The per-channel volume level of the session, which clients can control through the methods in the <a href="https://msdn.microsoft.com/0d0a20dc-5e5a-49a7-adc9-20aacb88368a">IChannelAudioVolume</a> interface.</li>
<li>The master volume level of the session, which clients can control through the methods in the <a href="https://msdn.microsoft.com/360211f2-de82-4ff5-896c-dee1d60cb7b7">ISimpleAudioVolume</a> interface.</li>
<li>The policy-based volume level of the session, which the system dynamically assigns to the session as the global mix changes.</li>
</ul>
Each of the four volume-level factors in the preceding list is a value in the range 0.0 to 1.0, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). The effective volume level is also a value in the range 0.0 to 1.0.

When releasing an <b>IAudioStreamVolume</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

The <b>IAudioStreamVolume</b> interface controls the channel volumes in a shared-mode audio stream. This interface does not work with exclusive-mode streams. For information about volume controls for exclusive-mode streams, see <a href="https://msdn.microsoft.com/1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79">EndpointVolume API</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioStreamVolume</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioStreamVolume</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6469ae01-d84d-4711-9b1e-cd8e685fcdd8">GetAllVolumes</a>
</td>
<td align="left" width="63%">
Retrieves the volume levels for all the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caaa8233-c995-4ba9-b973-f1b8737e7218">GetChannelCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of channels contained in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5ac2c9a-2bbd-42de-b530-f668b26300af">GetChannelVolume</a>
</td>
<td align="left" width="63%">
Retrieves the volume level for the specified channel in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eabbc37-a0f6-4e56-b68d-18e634d65394">SetAllVolumes</a>
</td>
<td align="left" width="63%">
Sets the individual volume levels for all the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49452b32-5ad0-446b-b237-2f17d60ff3f0">SetChannelVolume</a>
</td>
<td align="left" width="63%">
Sets the volume level for the specified channel in the audio stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a>



<a href="https://msdn.microsoft.com/0d0a20dc-5e5a-49a7-adc9-20aacb88368a">IChannelAudioVolume Interface</a>



<a href="https://msdn.microsoft.com/360211f2-de82-4ff5-896c-dee1d60cb7b7">ISimpleAudioVolume Interface</a>



<a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a>
 

 

