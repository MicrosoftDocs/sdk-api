---
UID: NF:audioclient.IAudioStreamVolume.SetChannelVolume
title: IAudioStreamVolume::SetChannelVolume
author: windows-sdk-content
description: The SetChannelVolume method sets the volume level for the specified channel in the audio stream.
old-location: coreaudio\iaudiostreamvolume_setchannelvolume.htm
old-project: CoreAudio
ms.assetid: 49452b32-5ad0-446b-b237-2f17d60ff3f0
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IAudioStreamVolume interface [Core Audio],SetChannelVolume method, IAudioStreamVolume.SetChannelVolume, IAudioStreamVolume::SetChannelVolume, IAudioStreamVolumeSetChannelVolume, SetChannelVolume, SetChannelVolume method [Core Audio], SetChannelVolume method [Core Audio],IAudioStreamVolume interface, audioclient/IAudioStreamVolume::SetChannelVolume, coreaudio.iaudiostreamvolume_setchannelvolume
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Audioclient.h
api_name:
-	IAudioStreamVolume.SetChannelVolume
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioStreamVolume::SetChannelVolume


## -description



The <b>SetChannelVolume</b> method sets the volume level for the specified channel in the audio stream.




## -parameters




### -param dwIndex [in]

The channel number. If the stream format has <i>N</i> channels, the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels, call the <a href="https://msdn.microsoft.com/caaa8233-c995-4ba9-b973-f1b8737e7218">IAudioStreamVolume::GetChannelCount</a> method.


### -param fLevel [in]

The volume level for the channel. Valid volume levels are in the range 0.0 to 1.0.


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
Parameter <i>dwIndex</i> is set to an invalid channel number, or parameter <i>fLevel</i> is not in the range 0.0 to 1.0.

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
 




## -see-also




<a href="https://msdn.microsoft.com/92cc127b-77ac-4fc7-ac3c-319e5d6368d3">IAudioStreamVolume Interface</a>



<a href="https://msdn.microsoft.com/caaa8233-c995-4ba9-b973-f1b8737e7218">IAudioStreamVolume::GetChannelCount</a>
 

 

