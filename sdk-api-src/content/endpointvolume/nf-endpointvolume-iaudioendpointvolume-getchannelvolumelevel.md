---
UID: NF:endpointvolume.IAudioEndpointVolume.GetChannelVolumeLevel
title: IAudioEndpointVolume::GetChannelVolumeLevel (endpointvolume.h)
description: The GetChannelVolumeLevel method gets the volume level, in decibels, of the specified channel in the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["GetChannelVolumeLevel","GetChannelVolumeLevel method [Core Audio]","GetChannelVolumeLevel method [Core Audio]","IAudioEndpointVolume interface","IAudioEndpointVolume interface [Core Audio]","GetChannelVolumeLevel method","IAudioEndpointVolume.GetChannelVolumeLevel","IAudioEndpointVolume::GetChannelVolumeLevel","IAudioEndpointVolumeGetChannelVolumeLevel","coreaudio.iaudioendpointvolume_getchannelvolumelevel","endpointvolume/IAudioEndpointVolume::GetChannelVolumeLevel"]
old-location: coreaudio\iaudioendpointvolume_getchannelvolumelevel.htm
tech.root: CoreAudio
ms.assetid: 3c5b594f-60b5-4172-8e4e-440b51cb13f4
ms.date: 12/05/2018
ms.keywords: GetChannelVolumeLevel, GetChannelVolumeLevel method [Core Audio], GetChannelVolumeLevel method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetChannelVolumeLevel method, IAudioEndpointVolume.GetChannelVolumeLevel, IAudioEndpointVolume::GetChannelVolumeLevel, IAudioEndpointVolumeGetChannelVolumeLevel, coreaudio.iaudioendpointvolume_getchannelvolumelevel, endpointvolume/IAudioEndpointVolume::GetChannelVolumeLevel
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpointVolume::GetChannelVolumeLevel
 - endpointvolume/IAudioEndpointVolume::GetChannelVolumeLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.GetChannelVolumeLevel
---

# IAudioEndpointVolume::GetChannelVolumeLevel


## -description

The <b>GetChannelVolumeLevel</b> method gets the volume level, in decibels, of the specified channel in the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param nChannel [in]

The channel number. If the audio stream has <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To obtain the number of channels in the stream, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">IAudioEndpointVolume::GetChannelCount</a> method.

### -param pfLevelDB [out]

Pointer to a <b>float</b> variable into which the method writes the volume level in decibels. To get the range of volume levels obtained from this method, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a> method.

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

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">IAudioEndpointVolume::GetChannelCount</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a>