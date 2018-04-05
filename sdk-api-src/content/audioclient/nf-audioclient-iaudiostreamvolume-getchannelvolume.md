---
UID: NF:audioclient.IAudioStreamVolume.GetChannelVolume
title: IAudioStreamVolume::GetChannelVolume method
author: windows-driver-content
description: The GetChannelVolume method retrieves the volume level for the specified channel in the audio stream.
old-location: coreaudio\iaudiostreamvolume_getchannelvolume.htm
old-project: CoreAudio
ms.assetid: a5ac2c9a-2bbd-42de-b530-f668b26300af
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetChannelVolume method [Core Audio], GetChannelVolume method [Core Audio], IAudioStreamVolume interface, GetChannelVolume,IAudioStreamVolume.GetChannelVolume, IAudioStreamVolume, IAudioStreamVolume interface [Core Audio], GetChannelVolume method, IAudioStreamVolume::GetChannelVolume, IAudioStreamVolumeGetChannelVolume, audioclient/IAudioStreamVolume::GetChannelVolume, coreaudio.iaudiostreamvolume_getchannelvolume
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioclient.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Audioclient.h
api_name:
-	IAudioStreamVolume.GetChannelVolume
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioStreamVolume::GetChannelVolume method


## -description



The <b>GetChannelVolume</b> method retrieves the volume level for the specified channel in the audio stream.




## -parameters




### -param dwIndex [in]

The channel number. If the stream format has <i>N</i> channels, then the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels, call the <a href="https://msdn.microsoft.com/caaa8233-c995-4ba9-b973-f1b8737e7218">IAudioStreamVolume::GetChannelCount</a> method.


### -param pfLevel [out]

Pointer to a <b>float</b> variable into which the method writes the volume level of the specified channel. The volume level is in the range 0.0 to 1.0.


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
Parameter <i>dwIndex</i> is set to an invalid channel number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pfLevel</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>
 




## -remarks



Clients can call the <a href="https://msdn.microsoft.com/2eabbc37-a0f6-4e56-b68d-18e634d65394">IAudioStreamVolume::SetAllVolumes</a> or <a href="https://msdn.microsoft.com/49452b32-5ad0-446b-b237-2f17d60ff3f0">IAudioStreamVolume::SetChannelVolume</a> method to set the per-channel volume levels in an audio stream.




## -see-also




<a href="https://msdn.microsoft.com/92cc127b-77ac-4fc7-ac3c-319e5d6368d3">IAudioStreamVolume Interface</a>



<a href="https://msdn.microsoft.com/caaa8233-c995-4ba9-b973-f1b8737e7218">IAudioStreamVolume::GetChannelCount</a>



<a href="https://msdn.microsoft.com/2eabbc37-a0f6-4e56-b68d-18e634d65394">IAudioStreamVolume::SetAllVolumes</a>



<a href="https://msdn.microsoft.com/49452b32-5ad0-446b-b237-2f17d60ff3f0">IAudioStreamVolume::SetChannelVolume</a>
 

 

