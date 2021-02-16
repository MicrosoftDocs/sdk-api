---
UID: NF:endpointvolume.IAudioEndpointVolume.GetChannelVolumeLevelScalar
title: IAudioEndpointVolume::GetChannelVolumeLevelScalar (endpointvolume.h)
description: The GetChannelVolumeLevelScalar method gets the normalized, audio-tapered volume level of the specified channel of the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["GetChannelVolumeLevelScalar","GetChannelVolumeLevelScalar method [Core Audio]","GetChannelVolumeLevelScalar method [Core Audio]","IAudioEndpointVolume interface","IAudioEndpointVolume interface [Core Audio]","GetChannelVolumeLevelScalar method","IAudioEndpointVolume.GetChannelVolumeLevelScalar","IAudioEndpointVolume::GetChannelVolumeLevelScalar","IAudioEndpointVolumeGetChannelVolumeLevelScalar","coreaudio.iaudioendpointvolume_getchannelvolumelevelscalar","endpointvolume/IAudioEndpointVolume::GetChannelVolumeLevelScalar"]
old-location: coreaudio\iaudioendpointvolume_getchannelvolumelevelscalar.htm
tech.root: CoreAudio
ms.assetid: e33d0010-9ea4-4375-9f23-81309f800988
ms.date: 12/05/2018
ms.keywords: GetChannelVolumeLevelScalar, GetChannelVolumeLevelScalar method [Core Audio], GetChannelVolumeLevelScalar method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetChannelVolumeLevelScalar method, IAudioEndpointVolume.GetChannelVolumeLevelScalar, IAudioEndpointVolume::GetChannelVolumeLevelScalar, IAudioEndpointVolumeGetChannelVolumeLevelScalar, coreaudio.iaudioendpointvolume_getchannelvolumelevelscalar, endpointvolume/IAudioEndpointVolume::GetChannelVolumeLevelScalar
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
 - IAudioEndpointVolume::GetChannelVolumeLevelScalar
 - endpointvolume/IAudioEndpointVolume::GetChannelVolumeLevelScalar
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
 - IAudioEndpointVolume.GetChannelVolumeLevelScalar
---

# IAudioEndpointVolume::GetChannelVolumeLevelScalar


## -description

The <b>GetChannelVolumeLevelScalar</b> method gets the normalized, audio-tapered volume level of the specified channel of the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param nChannel [in]

The channel number. If the audio stream contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To obtain the number of channels, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">IAudioEndpointVolume::GetChannelCount</a> method.

### -param pfLevel [out]

Pointer to a <b>float</b> variable into which the method writes the volume level. The level is expressed as a normalized value in the range from 0.0 to 1.0.

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
Parameter <i>pfLevel</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The volume level is normalized to the range from 0.0 to 1.0, where 0.0 is the minimum volume level and 1.0 is the maximum level. Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve. Note that the shape of the curve might change in future versions of Windows. For more information about audio-tapered curves, see <a href="/windows/desktop/CoreAudio/audio-tapered-volume-controls">Audio-Tapered Volume Controls</a>.

The normalized volume levels that are retrieved by this method are suitable to represent the positions of volume controls in application windows and on-screen displays.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">IAudioEndpointVolume::GetChannelCount</a>