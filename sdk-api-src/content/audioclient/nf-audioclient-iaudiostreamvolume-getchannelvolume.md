---
UID: NF:audioclient.IAudioStreamVolume.GetChannelVolume
title: IAudioStreamVolume::GetChannelVolume (audioclient.h)
description: The GetChannelVolume method retrieves the volume level for the specified channel in the audio stream.
helpviewer_keywords: ["GetChannelVolume","GetChannelVolume method [Core Audio]","GetChannelVolume method [Core Audio]","IAudioStreamVolume interface","IAudioStreamVolume interface [Core Audio]","GetChannelVolume method","IAudioStreamVolume.GetChannelVolume","IAudioStreamVolume::GetChannelVolume","IAudioStreamVolumeGetChannelVolume","audioclient/IAudioStreamVolume::GetChannelVolume","coreaudio.iaudiostreamvolume_getchannelvolume"]
old-location: coreaudio\iaudiostreamvolume_getchannelvolume.htm
tech.root: CoreAudio
ms.assetid: a5ac2c9a-2bbd-42de-b530-f668b26300af
ms.date: 12/05/2018
ms.keywords: GetChannelVolume, GetChannelVolume method [Core Audio], GetChannelVolume method [Core Audio],IAudioStreamVolume interface, IAudioStreamVolume interface [Core Audio],GetChannelVolume method, IAudioStreamVolume.GetChannelVolume, IAudioStreamVolume::GetChannelVolume, IAudioStreamVolumeGetChannelVolume, audioclient/IAudioStreamVolume::GetChannelVolume, coreaudio.iaudiostreamvolume_getchannelvolume
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
 - IAudioStreamVolume::GetChannelVolume
 - audioclient/IAudioStreamVolume::GetChannelVolume
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
 - IAudioStreamVolume.GetChannelVolume
---

# IAudioStreamVolume::GetChannelVolume


## -description

The <b>GetChannelVolume</b> method retrieves the volume level for the specified channel in the audio stream.

## -parameters

### -param dwIndex [in]

The channel number. If the stream format has <i>N</i> channels, then the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels, call the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-getchannelcount">IAudioStreamVolume::GetChannelCount</a> method.

### -param pfLevel [out]

Pointer to a <b>float</b> variable into which the method writes the volume level of the specified channel. The volume level is in the range 0.0 to 1.0.

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
Parameter <i>dwIndex</i> is set to an invalid channel number.

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

Clients can call the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-setallvolumes">IAudioStreamVolume::SetAllVolumes</a> or <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-setchannelvolume">IAudioStreamVolume::SetChannelVolume</a> method to set the per-channel volume levels in an audio stream.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-getchannelcount">IAudioStreamVolume::GetChannelCount</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-setallvolumes">IAudioStreamVolume::SetAllVolumes</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiostreamvolume-setchannelvolume">IAudioStreamVolume::SetChannelVolume</a>