---
UID: NF:endpointvolume.IAudioEndpointVolume.SetChannelVolumeLevel
title: IAudioEndpointVolume::SetChannelVolumeLevel
author: windows-sdk-content
description: The SetChannelVolumeLevel method sets the volume level, in decibels, of the specified channel of the audio stream that enters or leaves the audio endpoint device.
old-location: coreaudio\iaudioendpointvolume_setchannelvolumelevel.htm
old-project: CoreAudio
ms.assetid: 51f3b4dd-be9d-4b83-8605-a9962c6709a3
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],SetChannelVolumeLevel method, IAudioEndpointVolume.SetChannelVolumeLevel, IAudioEndpointVolume::SetChannelVolumeLevel, IAudioEndpointVolumeSetChannelVolumeLevel, SetChannelVolumeLevel, SetChannelVolumeLevel method [Core Audio], SetChannelVolumeLevel method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_setchannelvolumelevel, endpointvolume/IAudioEndpointVolume::SetChannelVolumeLevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: endpointvolume.h
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
tech.root: 
req.typenames: ProtType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.SetChannelVolumeLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAudioEndpointVolume::SetChannelVolumeLevel


## -description



The <b>SetChannelVolumeLevel</b> method sets the volume level, in decibels, of the specified channel of the audio stream that enters or leaves the audio endpoint device.




## -parameters




### -param nChannel [in]

The channel number. If the audio stream contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To obtain the number of channels, call the <a href="https://msdn.microsoft.com/83fd9afe-9bca-4569-a705-0e366b56522e">IAudioEndpointVolume::GetChannelCount</a> method.


### -param fLevelDB [in]

The new volume level in decibels. To obtain the range and granularity of the volume levels that can be set by this method, call the <a href="https://msdn.microsoft.com/a0e98ed8-36e2-4abc-aa83-008cc89e3a56">IAudioEndpointVolume::GetVolumeRange</a> method.


### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetChannelVolumeLevel</b> call changes the volume level of the endpoint, all clients that have registered <a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback</a> interfaces with that endpoint will receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the volume-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the notification routine receives the context GUID value GUID_NULL.


## -returns



If the method succeeds, it returns S_OK. If the method fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nChannel</i> is greater than or equal to the number of channels in the stream; or parameter <i>fLevelDB</i> lies outside of the volume range supported by the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



If volume level <i>fLevelDB</i> falls outside of the volume range reported by the <b>IAudioEndpointVolume::GetVolumeRange</b> method, the <b>SetChannelVolumeLevel</b> call fails and returns error code E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/83fd9afe-9bca-4569-a705-0e366b56522e">IAudioEndpointVolume::GetChannelCount</a>



<a href="https://msdn.microsoft.com/a0e98ed8-36e2-4abc-aa83-008cc89e3a56">IAudioEndpointVolume::GetVolumeRange</a>



<a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback Interface</a>



<a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a>
 

 

