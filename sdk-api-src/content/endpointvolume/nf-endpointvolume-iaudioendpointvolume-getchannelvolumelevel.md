---
UID: NF:endpointvolume.IAudioEndpointVolume.GetChannelVolumeLevel
title: IAudioEndpointVolume::GetChannelVolumeLevel
author: windows-sdk-content
description: The GetChannelVolumeLevel method gets the volume level, in decibels, of the specified channel in the audio stream that enters or leaves the audio endpoint device.
old-location: coreaudio\iaudioendpointvolume_getchannelvolumelevel.htm
tech.root: CoreAudio
ms.assetid: 3c5b594f-60b5-4172-8e4e-440b51cb13f4
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetChannelVolumeLevel, GetChannelVolumeLevel method [Core Audio], GetChannelVolumeLevel method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetChannelVolumeLevel method, IAudioEndpointVolume.GetChannelVolumeLevel, IAudioEndpointVolume::GetChannelVolumeLevel, IAudioEndpointVolumeGetChannelVolumeLevel, coreaudio.iaudioendpointvolume_getchannelvolumelevel, endpointvolume/IAudioEndpointVolume::GetChannelVolumeLevel
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.GetChannelVolumeLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointVolume::GetChannelVolumeLevel


## -description



The <b>GetChannelVolumeLevel</b> method gets the volume level, in decibels, of the specified channel in the audio stream that enters or leaves the audio endpoint device.




## -parameters




### -param nChannel [in]

The channel number. If the audio stream has <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To obtain the number of channels in the stream, call the <a href="https://msdn.microsoft.com/83fd9afe-9bca-4569-a705-0e366b56522e">IAudioEndpointVolume::GetChannelCount</a> method.


### -param pfLevelDB [out]

Pointer to a <b>float</b> variable into which the method writes the volume level in decibels. To get the range of volume levels obtained from this method, call the <a href="https://msdn.microsoft.com/a0e98ed8-36e2-4abc-aa83-008cc89e3a56">IAudioEndpointVolume::GetVolumeRange</a> method.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

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
Parameter <i>nChannel</i> is greater than or equal to the number of channels in the stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pfLevelDB</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/83fd9afe-9bca-4569-a705-0e366b56522e">IAudioEndpointVolume::GetChannelCount</a>



<a href="https://msdn.microsoft.com/a0e98ed8-36e2-4abc-aa83-008cc89e3a56">IAudioEndpointVolume::GetVolumeRange</a>
 

 

