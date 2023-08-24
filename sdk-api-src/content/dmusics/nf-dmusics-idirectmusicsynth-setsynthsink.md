---
UID: NF:dmusics.IDirectMusicSynth.SetSynthSink
title: IDirectMusicSynth::SetSynthSink (dmusics.h)
description: The SetSynthSink method establishes the connection of the synth to the wave sink.
helpviewer_keywords: ["IDirectMusicSynth interface [Audio Devices]","SetSynthSink method","IDirectMusicSynth.SetSynthSink","IDirectMusicSynth::SetSynthSink","SetSynthSink","SetSynthSink method [Audio Devices]","SetSynthSink method [Audio Devices]","IDirectMusicSynth interface","audio.idirectmusicsynth_setsynthsink","audmp-routines_4a1e1c4d-af5d-4141-8740-308cf711184e.xml","dmusics/IDirectMusicSynth::SetSynthSink"]
old-location: audio\idirectmusicsynth_setsynthsink.htm
tech.root: dshow
ms.assetid: 51153ea3-7c61-458a-8879-10efbd678b53
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],SetSynthSink method, IDirectMusicSynth.SetSynthSink, IDirectMusicSynth::SetSynthSink, SetSynthSink, SetSynthSink method [Audio Devices], SetSynthSink method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_setsynthsink, audmp-routines_4a1e1c4d-af5d-4141-8740-308cf711184e.xml, dmusics/IDirectMusicSynth::SetSynthSink
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
 - IDirectMusicSynth::SetSynthSink
 - dmusics/IDirectMusicSynth::SetSynthSink
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
 - IDirectMusicSynth.SetSynthSink
archived: true
---

# IDirectMusicSynth::SetSynthSink


## -description

The <code>SetSynthSink</code> method establishes the connection of the synth to the wave sink.

## -parameters

### -param pSynthSink

Pointer to the synth sink. This parameter either points to the <a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a> sink object to connect to the synth, or is <b>NULL</b> to disconnect the synth from its current synth sink.

## -returns

<code>SetSynthSink</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates that a bad pointer was passed in <i>pSynthSink</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method failed because it was unable to connect to the <b>IDirectMusicSynthSink</b> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that not enough memory is available to establish the connection.

</td>
</tr>
</table>

## -remarks

Before the synthesizer can expose much of its functionality, it must be connected to a wave sink object, which is represented by the <b>IDirectMusicSynthSink</b> interface. The <code>IDirectMusicSynth::SetSynthSink</code> method establishes this connection.

The <b>IDirectMusicSynthSink</b> object does the work of actually connecting up to the ultimate audio destination, which might be DirectSound, Microsoft Win32 wave audio, or some other audio stream. The default implementation sends data to DirectSound.

This approach allows a synthesizer to connect to many different styles of audio out without special code within the synthesizer itself. This makes it very easy to connect one synthesizer implementation to any available wave-output device.

For more information, see the description of the <b>IDirectMusic</b> interface in the Microsoft Windows SDK documentation.

The <i>pSynthSink</i> parameter follows the <a href="/windows-hardware/drivers/audio/reference-counting-conventions-for-com-objects">reference-counting conventions for COM objects</a>.

## -see-also

<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a>