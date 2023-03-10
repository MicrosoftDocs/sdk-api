---
UID: NF:mfidl.IMFSimpleAudioVolume.GetMute
title: IMFSimpleAudioVolume::GetMute (mfidl.h)
description: Queries whether the audio is muted. (IMFSimpleAudioVolume.GetMute)
helpviewer_keywords: ["13907d3c-62c0-4cb8-8921-5a38a63d7d6e","GetMute","GetMute method [Media Foundation]","GetMute method [Media Foundation]","IMFSimpleAudioVolume interface","IMFSimpleAudioVolume interface [Media Foundation]","GetMute method","IMFSimpleAudioVolume.GetMute","IMFSimpleAudioVolume::GetMute","mf.imfsimpleaudiovolume_getmute","mfidl/IMFSimpleAudioVolume::GetMute"]
old-location: mf\imfsimpleaudiovolume_getmute.htm
tech.root: mf
ms.assetid: 13907d3c-62c0-4cb8-8921-5a38a63d7d6e
ms.date: 12/05/2018
ms.keywords: 13907d3c-62c0-4cb8-8921-5a38a63d7d6e, GetMute, GetMute method [Media Foundation], GetMute method [Media Foundation],IMFSimpleAudioVolume interface, IMFSimpleAudioVolume interface [Media Foundation],GetMute method, IMFSimpleAudioVolume.GetMute, IMFSimpleAudioVolume::GetMute, mf.imfsimpleaudiovolume_getmute, mfidl/IMFSimpleAudioVolume::GetMute
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
 - IMFSimpleAudioVolume::GetMute
 - mfidl/IMFSimpleAudioVolume::GetMute
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
 - IMFSimpleAudioVolume.GetMute
---

# IMFSimpleAudioVolume::GetMute


## -description

Queries whether the audio is muted.

## -parameters

### -param pbMute [out]

Receives a Boolean value. If <b>TRUE</b>, the audio is muted; otherwise, the audio is not muted.

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

Calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-setmastervolume">IMFSimpleAudioVolume::SetMasterVolume</a> to set the volume does not change whether the audio is muted.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume">IMFSimpleAudioVolume</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>
