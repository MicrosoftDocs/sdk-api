---
UID: NF:endpointvolume.IAudioEndpointVolumeEx.GetVolumeRangeChannel
title: IAudioEndpointVolumeEx::GetVolumeRangeChannel
author: windows-sdk-content
description: The GetVolumeRangeChannel method gets the volume range for a specified channel.
old-location: coreaudio\iaudioendpointvolumeex_getvolumerangechannel.htm
tech.root: CoreAudio
ms.assetid: 869fe1cc-aa32-45e5-899f-3ae0d0f1b256
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVolumeRangeChannel, GetVolumeRangeChannel method [Core Audio], GetVolumeRangeChannel method [Core Audio],IAudioEndpointVolumeEx interface, IAudioEndpointVolumeEx interface [Core Audio],GetVolumeRangeChannel method, IAudioEndpointVolumeEx.GetVolumeRangeChannel, IAudioEndpointVolumeEx::GetVolumeRangeChannel, coreaudio.iaudioendpointvolumeex_getvolumerangechannel, endpointvolume/IAudioEndpointVolumeEx::GetVolumeRangeChannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IAudioEndpointVolumeEx.GetVolumeRangeChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointVolumeEx::GetVolumeRangeChannel


## -description


The <b>GetVolumeRangeChannel</b> method gets the volume range for a specified channel.


## -parameters




### -param iChannel [in]

The channel number for which to get the volume range. If the audio stream has <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To obtain the number of channels in the stream, call the <a href="https://msdn.microsoft.com/83fd9afe-9bca-4569-a705-0e366b56522e">IAudioEndpointVolume::GetChannelCount</a> method.


### -param pflVolumeMindB [out]

Receives  the minimum volume level for the channel, in decibels.


### -param pflVolumeMaxdB [out]

Receives  the maximum volume level for the channel, in decibels.


### -param pflVolumeIncrementdB [out]

Receives the volume increment for the channel, in decibels.


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
 

 

