---
UID: NF:audioclient.IAudioStreamVolume.GetChannelCount
title: IAudioStreamVolume::GetChannelCount (audioclient.h)
description: The GetChannelCount method retrieves the number of channels in the audio stream.
helpviewer_keywords: ["GetChannelCount","GetChannelCount method [Core Audio]","GetChannelCount method [Core Audio]","IAudioStreamVolume interface","IAudioStreamVolume interface [Core Audio]","GetChannelCount method","IAudioStreamVolume.GetChannelCount","IAudioStreamVolume::GetChannelCount","IAudioStreamVolumeGetChannelCount","audioclient/IAudioStreamVolume::GetChannelCount","coreaudio.iaudiostreamvolume_getchannelcount"]
old-location: coreaudio\iaudiostreamvolume_getchannelcount.htm
tech.root: CoreAudio
ms.assetid: caaa8233-c995-4ba9-b973-f1b8737e7218
ms.date: 12/05/2018
ms.keywords: GetChannelCount, GetChannelCount method [Core Audio], GetChannelCount method [Core Audio],IAudioStreamVolume interface, IAudioStreamVolume interface [Core Audio],GetChannelCount method, IAudioStreamVolume.GetChannelCount, IAudioStreamVolume::GetChannelCount, IAudioStreamVolumeGetChannelCount, audioclient/IAudioStreamVolume::GetChannelCount, coreaudio.iaudiostreamvolume_getchannelcount
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
 - IAudioStreamVolume::GetChannelCount
 - audioclient/IAudioStreamVolume::GetChannelCount
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
 - IAudioStreamVolume.GetChannelCount
---

# IAudioStreamVolume::GetChannelCount


## -description

The <b>GetChannelCount</b> method retrieves the number of channels in the audio stream.

## -parameters

### -param pdwCount [out]

Pointer to a <b>UINT32</b> variable into which the method writes the channel count.

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
Parameter <i>pdwCount</i> is <b>NULL</b>.

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

Call this method to get the number of channels in the audio stream before calling any of the other methods in the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume</a> interface.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume Interface</a>