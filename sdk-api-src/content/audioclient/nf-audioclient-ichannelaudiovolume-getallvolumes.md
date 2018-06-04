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

# IChannelAudioVolume::GetAllVolumes


## -description



The <b>GetAllVolumes</b> method retrieves the volume levels for all the channels in the audio session.




## -parameters




### -param dwCount [in]

The number of elements in the <i>pfVolumes</i> array. The <i>dwCount</i> parameter must equal the number of channels in the stream format for the audio session. To get the number of channels, call the <a href="https://msdn.microsoft.com/e3149d02-b0a2-4bdd-af04-b94b063c784b">IChannelAudioVolume::GetChannelCount</a> method.


### -param pfVolumes [out]

Pointer to an array of volume levels for the channels in the audio session. This parameter points to a caller-allocated <b>float</b> array into which the method writes the volume levels for the individual channels. Volume levels are in the range 0.0 to 1.0.


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
Parameter <i>dwCount</i> does not equal the number of channels in the stream format for the audio session.

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



Clients can call the <a href="https://msdn.microsoft.com/9081e814-d0b2-4b0e-9e4c-3590058e7196">IChannelAudioVolume::SetAllVolumes</a> or <a href="https://msdn.microsoft.com/b7baeebf-01d3-4dec-a674-73a84bbf7a66">IChannelAudioVolume::SetChannelVolume</a> method to set the per-channel volume levels in an audio session.




## -see-also




<a href="https://msdn.microsoft.com/0d0a20dc-5e5a-49a7-adc9-20aacb88368a">IChannelAudioVolume Interface</a>



<a href="https://msdn.microsoft.com/e3149d02-b0a2-4bdd-af04-b94b063c784b">IChannelAudioVolume::GetChannelCount</a>



<a href="https://msdn.microsoft.com/9081e814-d0b2-4b0e-9e4c-3590058e7196">IChannelAudioVolume::SetAllVolumes</a>



<a href="https://msdn.microsoft.com/b7baeebf-01d3-4dec-a674-73a84bbf7a66">IChannelAudioVolume::SetChannelVolume</a>
 

 

