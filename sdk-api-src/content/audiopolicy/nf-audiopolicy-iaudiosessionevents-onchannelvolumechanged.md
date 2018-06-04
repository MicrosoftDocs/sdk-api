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

# IAudioSessionEvents::OnChannelVolumeChanged


## -description



The <b>OnChannelVolumeChanged</b> method notifies the client that the volume level of an audio channel in the session submix has changed.




## -parameters




### -param ChannelCount [in]

The channel count. This parameter specifies the number of audio channels in the session submix.


### -param NewChannelVolumeArray




### -param ChangedChannel [in]

The number of the channel whose volume level changed. Use this value as an index into the <i>NewChannelVolumeArray</i> array. If the session submix contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. If more than one channel might have changed (for example, as a result of a call to the <a href="https://msdn.microsoft.com/9081e814-d0b2-4b0e-9e4c-3590058e7196">IChannelAudioVolume::SetAllVolumes</a> method), the value of <i>ChangedChannel</i> is (<b>DWORD</b>)(–1).


### -param EventContext [in]

The event context value. This is the same value that the caller passed to the <a href="https://msdn.microsoft.com/b7baeebf-01d3-4dec-a674-73a84bbf7a66">IChannelAudioVolume::SetChannelVolume</a> or <b>IChannelAudioVolume::SetAllVolumes</b> method in the call that initiated the change in volume level of the channel. For more information, see Remarks.


#### - NewChannelVolumeArray[] [in]

Pointer to an array of volume levels. Each element is a value of type <b>float</b> that specifies the volume level for a particular channel. Each volume level is a value in the range 0.0 to 1.0, where 0.0 is silence and 1.0 is full volume (no attenuation). The number of elements in the array is specified by the <i>ChannelCount</i> parameter. If an audio stream contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. The array element whose index matches the channel number, contains the volume level for that channel. Assume that the array remains valid only for the duration of the call.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The session manager calls this method each time a call to the <b>IChannelAudioVolume::SetChannelVolume</b> or <b>IChannelAudioVolume::SetAllVolumes</b> method successfully updates the volume level of one or more channels in the session submix. Note that the <b>OnChannelVolumeChanged</b> call occurs regardless of whether the new channel volume level or levels differ in value from the previous channel volume level or levels.

The <i>EventContext</i> parameter provides a means for a client to distinguish between a channel-volume change that it initiated and one that some other client initiated. When calling the <b>IChannelAudioVolume::SetChannelVolume</b> or <b>IChannelAudioVolume::SetAllVolumes</b> method, a client passes in an <i>EventContext</i> parameter value that its implementation of the <b>OnChannelVolumeChanged</b> method can recognize.

For a code example that implements the methods in the <b>IAudioSessionEvents</b> interface, see <a href="https://msdn.microsoft.com/6943b405-0807-412b-a149-fc3a8ece1b48">Audio Session Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents Interface</a>



<a href="https://msdn.microsoft.com/9081e814-d0b2-4b0e-9e4c-3590058e7196">IChannelAudioVolume::SetAllVolumes</a>



<a href="https://msdn.microsoft.com/b7baeebf-01d3-4dec-a674-73a84bbf7a66">IChannelAudioVolume::SetChannelVolume</a>
 

 

