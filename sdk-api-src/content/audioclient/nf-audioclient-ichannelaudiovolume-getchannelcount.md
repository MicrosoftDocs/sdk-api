---
UID: NF:audioclient.IChannelAudioVolume.GetChannelCount
title: IChannelAudioVolume::GetChannelCount (audioclient.h)
description: The GetChannelCount method retrieves the number of channels in the stream format for the audio session.
helpviewer_keywords: ["GetChannelCount","GetChannelCount method [Core Audio]","GetChannelCount method [Core Audio]","IChannelAudioVolume interface","IChannelAudioVolume interface [Core Audio]","GetChannelCount method","IChannelAudioVolume.GetChannelCount","IChannelAudioVolume::GetChannelCount","IChannelAudioVolumeGetChannelCount","audioclient/IChannelAudioVolume::GetChannelCount","coreaudio.ichannelaudiovolume_getchannelcount"]
old-location: coreaudio\ichannelaudiovolume_getchannelcount.htm
tech.root: CoreAudio
ms.assetid: e3149d02-b0a2-4bdd-af04-b94b063c784b
ms.date: 12/05/2018
ms.keywords: GetChannelCount, GetChannelCount method [Core Audio], GetChannelCount method [Core Audio],IChannelAudioVolume interface, IChannelAudioVolume interface [Core Audio],GetChannelCount method, IChannelAudioVolume.GetChannelCount, IChannelAudioVolume::GetChannelCount, IChannelAudioVolumeGetChannelCount, audioclient/IChannelAudioVolume::GetChannelCount, coreaudio.ichannelaudiovolume_getchannelcount
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
 - IChannelAudioVolume::GetChannelCount
 - audioclient/IChannelAudioVolume::GetChannelCount
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
 - IChannelAudioVolume.GetChannelCount
---

# IChannelAudioVolume::GetChannelCount


## -description

The <b>GetChannelCount</b> method retrieves the number of channels in the stream format for the audio session.

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

Call this method to get the number of channels in the audio session before calling any of the other methods in the <a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume</a> interface.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume Interface</a>