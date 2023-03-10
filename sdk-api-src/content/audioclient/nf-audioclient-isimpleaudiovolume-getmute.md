---
UID: NF:audioclient.ISimpleAudioVolume.GetMute
title: ISimpleAudioVolume::GetMute (audioclient.h)
description: The GetMute method retrieves the current muting state for the audio session.
helpviewer_keywords: ["GetMute","GetMute method [Core Audio]","GetMute method [Core Audio]","ISimpleAudioVolume interface","ISimpleAudioVolume interface [Core Audio]","GetMute method","ISimpleAudioVolume.GetMute","ISimpleAudioVolume::GetMute","ISimpleAudioVolumeGetMute","audioclient/ISimpleAudioVolume::GetMute","coreaudio.isimpleaudiovolume_getmute"]
old-location: coreaudio\isimpleaudiovolume_getmute.htm
tech.root: CoreAudio
ms.assetid: 35890423-2aac-473b-a820-ba7cb1b5e05e
ms.date: 12/05/2018
ms.keywords: GetMute, GetMute method [Core Audio], GetMute method [Core Audio],ISimpleAudioVolume interface, ISimpleAudioVolume interface [Core Audio],GetMute method, ISimpleAudioVolume.GetMute, ISimpleAudioVolume::GetMute, ISimpleAudioVolumeGetMute, audioclient/ISimpleAudioVolume::GetMute, coreaudio.isimpleaudiovolume_getmute
req.header: audioclient.h
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
 - ISimpleAudioVolume::GetMute
 - audioclient/ISimpleAudioVolume::GetMute
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
 - ISimpleAudioVolume.GetMute
---

# ISimpleAudioVolume::GetMute


## -description

The <b>GetMute</b> method retrieves the current muting state for the audio session.

## -parameters

### -param pbMute [out]

Pointer to a <b>BOOL</b> variable into which the method writes the muting state. <b>TRUE</b> indicates that muting is enabled. <b>FALSE</b> indicates that it is disabled.

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
Parameter <i>pbMute</i> is <b>NULL</b>.

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

<a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmute">ISimpleAudioVolume::SetMute</a>