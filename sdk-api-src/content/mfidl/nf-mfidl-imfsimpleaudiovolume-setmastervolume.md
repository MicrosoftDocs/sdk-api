---
UID: NF:mfidl.IMFSimpleAudioVolume.SetMasterVolume
title: IMFSimpleAudioVolume::SetMasterVolume (mfidl.h)
description: Sets the master volume level.
helpviewer_keywords: ["42b51817-3c2a-463a-a533-19c327c57354","IMFSimpleAudioVolume interface [Media Foundation]","SetMasterVolume method","IMFSimpleAudioVolume.SetMasterVolume","IMFSimpleAudioVolume::SetMasterVolume","SetMasterVolume","SetMasterVolume method [Media Foundation]","SetMasterVolume method [Media Foundation]","IMFSimpleAudioVolume interface","mf.imfsimpleaudiovolume_setmastervolume","mfidl/IMFSimpleAudioVolume::SetMasterVolume"]
old-location: mf\imfsimpleaudiovolume_setmastervolume.htm
tech.root: mf
ms.assetid: 42b51817-3c2a-463a-a533-19c327c57354
ms.date: 12/05/2018
ms.keywords: 42b51817-3c2a-463a-a533-19c327c57354, IMFSimpleAudioVolume interface [Media Foundation],SetMasterVolume method, IMFSimpleAudioVolume.SetMasterVolume, IMFSimpleAudioVolume::SetMasterVolume, SetMasterVolume, SetMasterVolume method [Media Foundation], SetMasterVolume method [Media Foundation],IMFSimpleAudioVolume interface, mf.imfsimpleaudiovolume_setmastervolume, mfidl/IMFSimpleAudioVolume::SetMasterVolume
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
 - IMFSimpleAudioVolume::SetMasterVolume
 - mfidl/IMFSimpleAudioVolume::SetMasterVolume
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
 - IMFSimpleAudioVolume.SetMasterVolume
---

# IMFSimpleAudioVolume::SetMasterVolume


## -description

Sets the master volume level.

## -parameters

### -param fLevel [in]

Volume level. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).

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

Events outside of the application can change the master volume level. For example, the user can change the volume from the system volume-control program (SndVol). If an external event changes the master volume, the audio renderer sends an <a href="/windows/desktop/medfound/meaudiosessionvolumechanged">MEAudioSessionVolumeChanged</a> event, which the Media Session forwards to the application.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume">IMFSimpleAudioVolume</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>