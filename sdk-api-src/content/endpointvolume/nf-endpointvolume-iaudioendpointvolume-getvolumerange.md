---
UID: NF:endpointvolume.IAudioEndpointVolume.GetVolumeRange
title: IAudioEndpointVolume::GetVolumeRange (endpointvolume.h)
description: The GetVolumeRange method gets the volume range, in decibels, of the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["GetVolumeRange","GetVolumeRange method [Core Audio]","GetVolumeRange method [Core Audio]","IAudioEndpointVolume interface","IAudioEndpointVolume interface [Core Audio]","GetVolumeRange method","IAudioEndpointVolume.GetVolumeRange","IAudioEndpointVolume::GetVolumeRange","IAudioEndpointVolumeGetVolumeRange","coreaudio.iaudioendpointvolume_getvolumerange","endpointvolume/IAudioEndpointVolume::GetVolumeRange"]
old-location: coreaudio\iaudioendpointvolume_getvolumerange.htm
tech.root: CoreAudio
ms.assetid: a0e98ed8-36e2-4abc-aa83-008cc89e3a56
ms.date: 12/05/2018
ms.keywords: GetVolumeRange, GetVolumeRange method [Core Audio], GetVolumeRange method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetVolumeRange method, IAudioEndpointVolume.GetVolumeRange, IAudioEndpointVolume::GetVolumeRange, IAudioEndpointVolumeGetVolumeRange, coreaudio.iaudioendpointvolume_getvolumerange, endpointvolume/IAudioEndpointVolume::GetVolumeRange
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
 - IAudioEndpointVolume::GetVolumeRange
 - endpointvolume/IAudioEndpointVolume::GetVolumeRange
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
 - IAudioEndpointVolume.GetVolumeRange
---

# IAudioEndpointVolume::GetVolumeRange


## -description

The <b>GetVolumeRange</b> method gets the volume range, in decibels, of the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param pflVolumeMindB [out]

Pointer to the minimum volume level. This parameter points to a <b>float</b> variable into which the method writes the minimum volume level in decibels. This value remains constant for the lifetime of the <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a> interface instance.

### -param pflVolumeMaxdB [out]

Pointer to the maximum volume level. This parameter points to a <b>float</b> variable into which the method writes the maximum volume level in decibels. This value remains constant for the lifetime of the <b>IAudioEndpointVolume</b> interface instance.

### -param pflVolumeIncrementdB [out]

Pointer to the volume increment. This parameter points to a <b>float</b> variable into which the method writes the volume increment in decibels. This increment remains constant for the lifetime of the <b>IAudioEndpointVolume</b> interface instance.

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

## -remarks

The volume range from vmin = <i>*pfLevelMinDB</i> to vmax = <i>*pfLevelMaxDB</i> is divided into <i>n</i> uniform intervals of size vinc = <i>*pfVolumeIncrementDB</i>, where

n = (vmax – vmin) / vinc.

The values vmin, vmax, and vinc are measured in decibels. The client can set the volume level to one of n + 1 discrete values in the range from vmin to vmax.
      

The <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel">IAudioEndpointVolume::SetChannelVolumeLevel</a> and <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel">IAudioEndpointVolume::SetMasterVolumeLevel</a> methods accept only volume levels in the range from vmin to vmax. If the caller specifies a volume level outside of this range, the method fails and returns E_INVALIDARG. If the caller specifies a volume level that falls between two steps in the volume range, the method sets the endpoint volume level to the step that lies closest to the requested volume level and returns S_OK. However, a subsequent call to <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel">IAudioEndpointVolume::GetChannelVolumeLevel</a> or <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel">IAudioEndpointVolume::GetMasterVolumeLevel</a> retrieves the volume level requested by the previous call to <b>SetChannelVolumeLevel</b> or <b>SetMasterVolumeLevel</b>, not the step value.

If the volume control is implemented in hardware, <b>GetVolumeRange</b> describes the range and granularity of the hardware volume settings. In contrast, the steps that are reported by the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo">IEndpointVolume::GetVolumeStepInfo</a> method correspond to points on an audio-tapered curve that are calculated in software by the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown">IEndpointVolume::VolumeStepDown</a> and <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup">IEndpointVolume::VolumeStepUp</a> methods. Either method first calculates the idealized volume level that corresponds to the next point on the curve. Next, the method selects the hardware volume setting that is the best approximation to the idealized level. For more information about audio-tapered curves, see <a href="/windows/desktop/CoreAudio/audio-tapered-volume-controls">Audio-Tapered Volume Controls</a>.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel">IAudioEndpointVolume::GetChannelVolumeLevel</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel">IAudioEndpointVolume::GetMasterVolumeLevel</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel">IAudioEndpointVolume::SetChannelVolumeLevel</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel">IAudioEndpointVolume::SetMasterVolumeLevel</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo">IEndpointVolume::GetVolumeStepInfo</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown">IEndpointVolume::VolumeStepDown</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup">IEndpointVolume::VolumeStepUp</a>