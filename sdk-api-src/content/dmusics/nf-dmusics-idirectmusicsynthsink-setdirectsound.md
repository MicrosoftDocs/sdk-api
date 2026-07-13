---
UID: NF:dmusics.IDirectMusicSynthSink.SetDirectSound
title: IDirectMusicSynthSink::SetDirectSound (dmusics.h)
description: The SetDirectSound method connects the synthesizer sink with an existing DirectSound object and a DirectSound buffer.
helpviewer_keywords: ["IDirectMusicSynthSink interface [Audio Devices]","SetDirectSound method","IDirectMusicSynthSink.SetDirectSound","IDirectMusicSynthSink::SetDirectSound","SetDirectSound","SetDirectSound method [Audio Devices]","SetDirectSound method [Audio Devices]","IDirectMusicSynthSink interface","audio.idirectmusicsynthsink_setdirectsound","audmp-routines_6c018b77-9478-4754-b40e-428ba758f7dc.xml","dmusics/IDirectMusicSynthSink::SetDirectSound"]
old-location: audio\idirectmusicsynthsink_setdirectsound.htm
tech.root: dshow
ms.assetid: 879292e1-b8e9-4f11-bb3d-f92c18e915e2
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynthSink interface [Audio Devices],SetDirectSound method, IDirectMusicSynthSink.SetDirectSound, IDirectMusicSynthSink::SetDirectSound, SetDirectSound, SetDirectSound method [Audio Devices], SetDirectSound method [Audio Devices],IDirectMusicSynthSink interface, audio.idirectmusicsynthsink_setdirectsound, audmp-routines_6c018b77-9478-4754-b40e-428ba758f7dc.xml, dmusics/IDirectMusicSynthSink::SetDirectSound
req.header: dmusics.h
req.include-header: Dmusics.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDirectMusicSynthSink::SetDirectSound
 - dmusics/IDirectMusicSynthSink::SetDirectSound
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusics.h
api_name:
 - IDirectMusicSynthSink.SetDirectSound
archived: true
---

# IDirectMusicSynthSink::SetDirectSound


## -description

The <code>SetDirectSound</code> method connects the synthesizer sink with an existing DirectSound object and a DirectSound buffer.

## -parameters

### -param pDirectSound

Pointer to an <b>IDirectSound</b> object that the sink is to be associated with. This parameter is set to a valid, non-<b>NULL</b> pointer value.

### -param pDirectSoundBuffer

Pointer to the <b>IDirectSoundBuffer</b> object that the sink is to be associated with. This parameter can be <b>NULL</b>. For more information, see the following Remarks section.

## -returns

<code>SetDirectSound</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the sink is active.

</td>
</tr>
</table>

## -remarks

The <i>pDirectSound</i> parameter points to an <b>IDirectSound</b> instance that is received from <code>IDirectMusicPort::SetDirectSound</code> and is non-<b>NULL</b>.

If <i>pDirectSoundBuffer</i> is <b>NULL</b>, the primary buffer for <b>IDirectSound</b> will be upgraded, if necessary, to support the sample rate and channel information for the sink (obtained from <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getformat">IDirectMusicSynth::GetFormat</a>).

The <b>IDirectSoundBuffer</b> should be a secondary streaming buffer with a format that matches the format obtained from the synthesizer. If <i>pDirectSoundBuffer</i> is <b>NULL</b>, then an appropriate <b>IDirectSoundBuffer</b> instance will be created internally.

Neither the <b>IDirectSound</b> nor the <b>IDirectSoundBuffer</b> instance can be changed once the sink has been activated.

The <i>pDirectSound</i> and <i>pDirectSoundBuffer</i> parameters follow the <a href="/windows-hardware/drivers/audio/reference-counting-conventions-for-com-objects">reference-counting conventions for COM objects</a>.

For more information, see the description of the <b>IDirectSound</b>, <b>IDirectSoundBuffer</b>, and <b>IDirectMusicPort</b> interfaces in the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getformat">IDirectMusicSynth::GetFormat</a>