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

# IAudioEndpointVolumeEx::GetVolumeRangeChannel


## -description


The <b>GetVolumeRangeChannel</b> method gets the volume range for a specified channel.


## -parameters




### -param iChannel [in]

The channel number for which to get the volume range. If the audio stream has <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To obtain the number of channels in the stream, call the <a href="https://msdn.microsoft.com/83fd9afe-9bca-4569-a705-0e366b56522e">IAudioEndpointVolume::GetChannelCount</a> method.


### -param pflVolumeMindB




### -param pflVolumeMaxdB




### -param pflVolumeIncrementdB






#### - pflVolumeIncrementDB [out]

Receives the volume increment for the channel, in decibels.


#### - pflVolumeMaxDB [out]

Receives  the maximum volume level for the channel, in decibels.


#### - pflVolumeMinDB [out]

Receives  the minimum volume level for the channel, in decibels.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pfLevelMinDB</i>, <i>pfLevelMaxDB</i>, or <i>pfVolumeIncrementDB</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/905ef0c9-ac32-4dfd-a25a-820cafa04815">IAudioEndpointVolumeEx</a>
 

 

