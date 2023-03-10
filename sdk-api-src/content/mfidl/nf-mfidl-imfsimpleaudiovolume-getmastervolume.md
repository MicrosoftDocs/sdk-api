---
UID: NF:mfidl.IMFSimpleAudioVolume.GetMasterVolume
title: IMFSimpleAudioVolume::GetMasterVolume (mfidl.h)
description: Retrieves the master volume level.
helpviewer_keywords: ["03ce097e-c4e5-4dac-84c0-b569efc420bc","GetMasterVolume","GetMasterVolume method [Media Foundation]","GetMasterVolume method [Media Foundation]","IMFSimpleAudioVolume interface","IMFSimpleAudioVolume interface [Media Foundation]","GetMasterVolume method","IMFSimpleAudioVolume.GetMasterVolume","IMFSimpleAudioVolume::GetMasterVolume","mf.imfsimpleaudiovolume_getmastervolume","mfidl/IMFSimpleAudioVolume::GetMasterVolume"]
old-location: mf\imfsimpleaudiovolume_getmastervolume.htm
tech.root: mf
ms.assetid: 03ce097e-c4e5-4dac-84c0-b569efc420bc
ms.date: 12/05/2018
ms.keywords: 03ce097e-c4e5-4dac-84c0-b569efc420bc, GetMasterVolume, GetMasterVolume method [Media Foundation], GetMasterVolume method [Media Foundation],IMFSimpleAudioVolume interface, IMFSimpleAudioVolume interface [Media Foundation],GetMasterVolume method, IMFSimpleAudioVolume.GetMasterVolume, IMFSimpleAudioVolume::GetMasterVolume, mf.imfsimpleaudiovolume_getmastervolume, mfidl/IMFSimpleAudioVolume::GetMasterVolume
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
 - IMFSimpleAudioVolume::GetMasterVolume
 - mfidl/IMFSimpleAudioVolume::GetMasterVolume
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
 - IMFSimpleAudioVolume.GetMasterVolume
---

# IMFSimpleAudioVolume::GetMasterVolume


## -description

Retrieves the master volume level.

## -parameters

### -param pfLevel [out]

Receives the volume level. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).

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

If an external event changes the master volume, the audio renderer sends an <a href="/windows/desktop/medfound/meaudiosessionvolumechanged">MEAudioSessionVolumeChanged</a> event, which the Media Session forwards to the application.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume">IMFSimpleAudioVolume</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>