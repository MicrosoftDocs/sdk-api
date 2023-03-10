---
UID: NF:endpointvolume.IAudioEndpointVolume.GetMasterVolumeLevelScalar
title: IAudioEndpointVolume::GetMasterVolumeLevelScalar (endpointvolume.h)
description: The GetMasterVolumeLevelScalar method gets the master volume level of the audio stream that enters or leaves the audio endpoint device. The volume level is expressed as a normalized, audio-tapered value in the range from 0.0 to 1.0.
helpviewer_keywords: ["GetMasterVolumeLevelScalar","GetMasterVolumeLevelScalar method [Core Audio]","GetMasterVolumeLevelScalar method [Core Audio]","IAudioEndpointVolume interface","IAudioEndpointVolume interface [Core Audio]","GetMasterVolumeLevelScalar method","IAudioEndpointVolume.GetMasterVolumeLevelScalar","IAudioEndpointVolume::GetMasterVolumeLevelScalar","IAudioEndpointVolumeGetMasterVolumeLevelScalar","coreaudio.iaudioendpointvolume_getmastervolumelevelscalar","endpointvolume/IAudioEndpointVolume::GetMasterVolumeLevelScalar"]
old-location: coreaudio\iaudioendpointvolume_getmastervolumelevelscalar.htm
tech.root: CoreAudio
ms.assetid: 5a127507-99d2-48e8-b7e9-8bb51ff89f50
ms.date: 12/05/2018
ms.keywords: GetMasterVolumeLevelScalar, GetMasterVolumeLevelScalar method [Core Audio], GetMasterVolumeLevelScalar method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetMasterVolumeLevelScalar method, IAudioEndpointVolume.GetMasterVolumeLevelScalar, IAudioEndpointVolume::GetMasterVolumeLevelScalar, IAudioEndpointVolumeGetMasterVolumeLevelScalar, coreaudio.iaudioendpointvolume_getmastervolumelevelscalar, endpointvolume/IAudioEndpointVolume::GetMasterVolumeLevelScalar
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
 - IAudioEndpointVolume::GetMasterVolumeLevelScalar
 - endpointvolume/IAudioEndpointVolume::GetMasterVolumeLevelScalar
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
 - IAudioEndpointVolume.GetMasterVolumeLevelScalar
---

# IAudioEndpointVolume::GetMasterVolumeLevelScalar


## -description

The <b>GetMasterVolumeLevelScalar</b> method gets the master volume level of the audio stream that enters or leaves the audio endpoint device. The volume level is expressed as a normalized, audio-tapered value in the range from 0.0 to 1.0.

## -parameters

### -param pfLevel [out]

Pointer to the master volume level. This parameter points to a <b>float</b> variable into which the method writes the volume level. The level is expressed as a normalized value in the range from 0.0 to 1.0.

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
Parameter <i>pfLevel</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The volume level is normalized to the range from 0.0 to 1.0, where 0.0 is the minimum volume level and 1.0 is the maximum level. Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve. Note that the shape of the curve might change in future versions of Windows. For more information about audio-tapered curves, see <a href="/windows/desktop/CoreAudio/audio-tapered-volume-controls">Audio-Tapered Volume Controls</a>.

The normalized volume levels that are retrieved by this method are suitable to represent the positions of volume controls in application windows and on-screen displays.

For a code example that calls <b>GetMasterVolumeLevelScalar</b>, see <a href="/windows/desktop/CoreAudio/endpoint-volume-controls">Endpoint Volume Controls</a>.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>