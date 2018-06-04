---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

