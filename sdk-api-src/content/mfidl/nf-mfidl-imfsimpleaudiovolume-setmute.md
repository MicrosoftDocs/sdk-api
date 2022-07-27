---
UID: NF:mfidl.IMFSimpleAudioVolume.SetMute
title: IMFSimpleAudioVolume::SetMute (mfidl.h)
description: Mutes or unmutes the audio. (IMFSimpleAudioVolume.SetMute)
helpviewer_keywords: ["IMFSimpleAudioVolume interface [Media Foundation]","SetMute method","IMFSimpleAudioVolume.SetMute","IMFSimpleAudioVolume::SetMute","SetMute","SetMute method [Media Foundation]","SetMute method [Media Foundation]","IMFSimpleAudioVolume interface","d8840d15-d4d5-481e-9002-54fdbf323c9c","mf.imfsimpleaudiovolume_setmute","mfidl/IMFSimpleAudioVolume::SetMute"]
old-location: mf\imfsimpleaudiovolume_setmute.htm
tech.root: mf
ms.assetid: d8840d15-d4d5-481e-9002-54fdbf323c9c
ms.date: 12/05/2018
ms.keywords: IMFSimpleAudioVolume interface [Media Foundation],SetMute method, IMFSimpleAudioVolume.SetMute, IMFSimpleAudioVolume::SetMute, SetMute, SetMute method [Media Foundation], SetMute method [Media Foundation],IMFSimpleAudioVolume interface, d8840d15-d4d5-481e-9002-54fdbf323c9c, mf.imfsimpleaudiovolume_setmute, mfidl/IMFSimpleAudioVolume::SetMute
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSimpleAudioVolume::SetMute
 - mfidl/IMFSimpleAudioVolume::SetMute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSimpleAudioVolume.SetMute
---

# IMFSimpleAudioVolume::SetMute


## -description

Mutes or unmutes the audio.

## -parameters

### -param bMute [in]

Specify <b>TRUE</b> to mute the audio, or <b>FALSE</b> to unmute the audio.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio renderer is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINK_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
The audio renderer was removed from the pipeline.

</td>
</tr>
</table>

## -remarks

This method does not change the volume level returned by the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume">IMFSimpleAudioVolume::GetMasterVolume</a> function.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume">IMFSimpleAudioVolume</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>
