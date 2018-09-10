---
UID: NF:audiopolicy.IAudioSessionEvents.OnSimpleVolumeChanged
title: IAudioSessionEvents::OnSimpleVolumeChanged
author: windows-sdk-content
description: The OnSimpleVolumeChanged method notifies the client that the volume level or muting state of the audio session has changed.
old-location: coreaudio\iaudiosessionevents_onsimplevolumechanged.htm
tech.root: CoreAudio
ms.assetid: e60e8996-3c01-4458-88f2-cd6cb118bd76
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnSimpleVolumeChanged method, IAudioSessionEvents.OnSimpleVolumeChanged, IAudioSessionEvents::OnSimpleVolumeChanged, IAudioSessionEventsOnSimpleVolumeChanged, OnSimpleVolumeChanged, OnSimpleVolumeChanged method [Core Audio], OnSimpleVolumeChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnSimpleVolumeChanged, coreaudio.iaudiosessionevents_onsimplevolumechanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audiopolicy.h
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
 - Audiopolicy.h
api_name:
 - IAudioSessionEvents.OnSimpleVolumeChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioSessionEvents::OnSimpleVolumeChanged


## -description



The <b>OnSimpleVolumeChanged</b> method notifies the client that the volume level or muting state of the audio session has changed.




## -parameters




### -param NewVolume [in]

The new volume level for the audio session. This parameter is a value in the range 0.0 to 1.0, where 0.0 is silence and 1.0 is full volume (no attenuation).


### -param NewMute [in]

The new muting state. If <b>TRUE</b>, muting is enabled. If <b>FALSE</b>, muting is disabled.


### -param EventContext [in]

The event context value. This is the same value that the caller passed to <a href="https://msdn.microsoft.com/895a8564-5f06-4e20-abcc-d960d4002eb0">ISimpleAudioVolume::SetMasterVolume</a> or <a href="https://msdn.microsoft.com/64fc7146-8d4b-429c-bf35-c43e31a41af8">ISimpleAudioVolume::SetMute</a> in the call that changed the volume level or muting state of the session. For more information, see Remarks.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The session manager calls this method each time a call to the <a href="https://msdn.microsoft.com/895a8564-5f06-4e20-abcc-d960d4002eb0">ISimpleAudioVolume::SetMasterVolume</a> or <a href="https://msdn.microsoft.com/64fc7146-8d4b-429c-bf35-c43e31a41af8">ISimpleAudioVolume::SetMute</a> method changes the volume level or muting state of the session.

The <i>EventContext</i> parameter provides a means for a client to distinguish between a volume or mute change that it initiated and one that some other client initiated. When calling the <a href="https://msdn.microsoft.com/895a8564-5f06-4e20-abcc-d960d4002eb0">ISimpleAudioVolume::SetMasterVolume</a> or <a href="https://msdn.microsoft.com/64fc7146-8d4b-429c-bf35-c43e31a41af8">ISimpleAudioVolume::SetMute</a> method, a client passes in an <i>EventContext</i> parameter value that its implementation of the <b>OnSimpleVolumeChanged</b> method can recognize.

For a code example that implements the methods in the <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface, see <a href="https://msdn.microsoft.com/6943b405-0807-412b-a149-fc3a8ece1b48">Audio Session Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents Interface</a>



<a href="https://msdn.microsoft.com/895a8564-5f06-4e20-abcc-d960d4002eb0">ISimpleAudioVolume::SetMasterVolume</a>



<a href="https://msdn.microsoft.com/64fc7146-8d4b-429c-bf35-c43e31a41af8">ISimpleAudioVolume::SetMute</a>
 

 

