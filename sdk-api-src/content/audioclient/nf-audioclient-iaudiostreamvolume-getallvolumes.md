---
UID: NF:audioclient.IAudioStreamVolume.GetAllVolumes
title: IAudioStreamVolume::GetAllVolumes
author: windows-sdk-content
description: The GetAllVolumes method retrieves the volume levels for all the channels in the audio stream.
old-location: coreaudio\iaudiostreamvolume_getallvolumes.htm
tech.root: CoreAudio
ms.assetid: 6469ae01-d84d-4711-9b1e-cd8e685fcdd8
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetAllVolumes, GetAllVolumes method [Core Audio], GetAllVolumes method [Core Audio],IAudioStreamVolume interface, IAudioStreamVolume interface [Core Audio],GetAllVolumes method, IAudioStreamVolume.GetAllVolumes, IAudioStreamVolume::GetAllVolumes, IAudioStreamVolumeGetAllVolumes, audioclient/IAudioStreamVolume::GetAllVolumes, coreaudio.iaudiostreamvolume_getallvolumes
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
 - IAudioStreamVolume.GetAllVolumes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- audioclient.h
: 
- IAudioStreamVolume.GetAllVolumes
: 
---

# IAudioStreamVolume::GetAllVolumes


## -description



The <b>GetAllVolumes</b> method retrieves the volume levels for all the channels in the audio stream.




## -parameters




### -param dwCount [in]

The number of elements in the <i>pfVolumes</i> array. The <i>dwCount</i> parameter must equal the number of channels in the stream format. To get the number of channels, call the <a href="https://msdn.microsoft.com/caaa8233-c995-4ba9-b973-f1b8737e7218">IAudioStreamVolume::GetChannelCount</a> method.


### -param pfVolumes [out]

Pointer to an array of volume levels for the channels in the audio stream. This parameter points to a caller-allocated <b>float</b> array into which the method writes the volume levels for the individual channels. Volume levels are in the range 0.0 to 1.0.


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
Parameter <i>dwCount</i> does not equal the number of channels in the stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pfVolumes</i> is <b>NULL</b>.

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
 

 

