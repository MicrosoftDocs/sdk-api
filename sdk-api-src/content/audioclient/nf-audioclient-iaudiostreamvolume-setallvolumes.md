---
UID: NF:audioclient.IAudioStreamVolume.SetAllVolumes
title: IAudioStreamVolume::SetAllVolumes (audioclient.h)
description: The SetAllVolumes method sets the individual volume levels for all the channels in the audio stream.
helpviewer_keywords: ["IAudioStreamVolume interface [Core Audio]","SetAllVolumes method","IAudioStreamVolume.SetAllVolumes","IAudioStreamVolume::SetAllVolumes","IAudioStreamVolumeSetAllVolumes","SetAllVolumes","SetAllVolumes method [Core Audio]","SetAllVolumes method [Core Audio]","IAudioStreamVolume interface","audioclient/IAudioStreamVolume::SetAllVolumes","coreaudio.iaudiostreamvolume_setallvolumes"]
old-location: coreaudio\iaudiostreamvolume_setallvolumes.htm
tech.root: CoreAudio
ms.assetid: 2eabbc37-a0f6-4e56-b68d-18e634d65394
ms.date: 12/05/2018
ms.keywords: IAudioStreamVolume interface [Core Audio],SetAllVolumes method, IAudioStreamVolume.SetAllVolumes, IAudioStreamVolume::SetAllVolumes, IAudioStreamVolumeSetAllVolumes, SetAllVolumes, SetAllVolumes method [Core Audio], SetAllVolumes method [Core Audio],IAudioStreamVolume interface, audioclient/IAudioStreamVolume::SetAllVolumes, coreaudio.iaudiostreamvolume_setallvolumes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioStreamVolume::SetAllVolumes
 - audioclient/IAudioStreamVolume::SetAllVolumes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioStreamVolume.SetAllVolumes
---

# IAudioStreamVolume::SetAllVolumes


## -description

The <b>SetAllVolumes</b> method sets the individual volume levels for all the channels in the audio stream.

## -parameters

### -param dwCount [in]

The number of elements in the <i>pfVolumes</i> array. This parameter must equal the number of channels in the stream format. To get the number of channels, call the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-getchannelcount">IAudioStreamVolume::GetChannelCount</a> method.

### -param pfVolumes [in]

Pointer to an array of volume levels for the channels in the audio stream. The number of elements in the <i>pfVolumes</i> array is specified by the <i>dwCount</i> parameter. The caller writes the volume level for each channel to the array element whose index matches the channel number. If the stream format has <i>N</i> channels, the channels are numbered from 0 to <i>N</i>– 1. Valid volume levels are in the range 0.0 to 1.0.

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
Parameter <i>dwCount</i> does not equal the number of channels in the stream, or the value of a <i>pfVolumes</i> array element is not in the range 0.0 to 1.0.

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

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-getchannelcount">IAudioStreamVolume::GetChannelCount</a>