---
UID: NN:audioclient.ISimpleAudioVolume
title: ISimpleAudioVolume
author: windows-sdk-content
description: The ISimpleAudioVolume interface enables a client to control the master volume level of an audio session.
old-location: coreaudio\isimpleaudiovolume.htm
old-project: CoreAudio
ms.assetid: 360211f2-de82-4ff5-896c-dee1d60cb7b7
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ISimpleAudioVolume, ISimpleAudioVolume interface [Core Audio], ISimpleAudioVolume interface [Core Audio],described, audioclient/ISimpleAudioVolume, coreaudio.isimpleaudiovolume
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - ISimpleAudioVolume
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISimpleAudioVolume interface


## -description



The <b>ISimpleAudioVolume</b> interface enables a client to control the master volume level of an <a href="https://msdn.microsoft.com/b8a1b656-a582-4112-99e9-bd575719ebb3">audio session</a>. The <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method initializes a stream object and assigns the stream to an audio session. The client obtains a reference to the <b>ISimpleAudioVolume</b> interface on a stream object by calling the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method with parameter <i>riid</i> set to <b>REFIID</b> IID_ISimpleAudioVolume.

Alternatively, a client can obtain the <b>ISimpleAudioVolume</b> interface of an existing session without having to first create a stream object and add the stream to the session. Instead, the client calls the <a href="https://msdn.microsoft.com/2f3c5a40-308f-48b4-b35c-aebd0cc6b849">IAudioSessionManager::GetSimpleAudioVolume</a> method with the session GUID.

The effective volume level of any channel in the session submix, as heard at the speakers, is the product of the following four volume-level factors:

<ul>
<li>The per-channel volume levels of the streams in the session, which clients can control through the methods in the <a href="https://msdn.microsoft.com/92cc127b-77ac-4fc7-ac3c-319e5d6368d3">IAudioStreamVolume</a> interface.</li>
<li>The master volume level of the session, which clients can control through the methods in the <b>ISimpleAudioVolume</b> interface.</li>
<li>The per-channel volume level of the session, which clients can control through the methods in the <a href="https://msdn.microsoft.com/0d0a20dc-5e5a-49a7-adc9-20aacb88368a">IChannelAudioVolume</a> interface.</li>
<li>The policy-based volume level of the session, which the system dynamically assigns to the session as the global mix changes.</li>
</ul>
Each of the four volume-level factors in the preceding list is a value in the range 0.0 to 1.0, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). The effective volume level is also a value in the range 0.0 to 1.0.

Typical audio applications do not modify the volume levels of sessions. Instead, they rely on users to set these volume levels through the Sndvol program. Sndvol modifies only the master volume levels of sessions. By default, the session manager sets the master volume level to 1.0 at the initial activation of a session. Subsequent volume changes by Sndvol or other clients are persistent across computer restarts.

When releasing an <b>ISimpleAudioVolume</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

The <b>ISimpleAudioVolume</b> interface controls the volume of an audio session. An audio session is a collection of shared-mode streams. This interface does not work with exclusive-mode streams. For information about volume controls for exclusive-mode streams, see <a href="https://msdn.microsoft.com/1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79">EndpointVolume API</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimpleAudioVolume</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISimpleAudioVolume</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimpleAudioVolume</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/362d8e12-a92c-4e0f-b88f-a3937c75d01a">GetMasterVolume</a>
</td>
<td align="left" width="63%">
Retrieves the client volume level for the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35890423-2aac-473b-a820-ba7cb1b5e05e">GetMute</a>
</td>
<td align="left" width="63%">
Retrieves the current muting state for the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/895a8564-5f06-4e20-abcc-d960d4002eb0">SetMasterVolume</a>
</td>
<td align="left" width="63%">
Sets the master volume level for the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64fc7146-8d4b-429c-bf35-c43e31a41af8">SetMute</a>
</td>
<td align="left" width="63%">
Sets the muting state for the audio session.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>



<a href="https://msdn.microsoft.com/92cc127b-77ac-4fc7-ac3c-319e5d6368d3">IAudioStreamVolume Interface</a>



<a href="https://msdn.microsoft.com/0d0a20dc-5e5a-49a7-adc9-20aacb88368a">IChannelAudioVolume Interface</a>



<a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a>
 

 

