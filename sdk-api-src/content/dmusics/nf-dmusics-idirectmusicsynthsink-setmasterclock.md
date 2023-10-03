---
UID: NF:dmusics.IDirectMusicSynthSink.SetMasterClock
title: IDirectMusicSynthSink::SetMasterClock (dmusics.h)
description: The SetMasterClock method provides the synth sink with a master time source, which is required for synchronization with the rest of DirectMusic.
helpviewer_keywords: ["IDirectMusicSynthSink interface [Audio Devices]","SetMasterClock method","IDirectMusicSynthSink.SetMasterClock","IDirectMusicSynthSink::SetMasterClock","SetMasterClock","SetMasterClock method [Audio Devices]","SetMasterClock method [Audio Devices]","IDirectMusicSynthSink interface","audio.idirectmusicsynthsink_setmasterclock","audmp-routines_45d219a0-1877-4a19-961f-6f3666bc9a1a.xml","dmusics/IDirectMusicSynthSink::SetMasterClock"]
old-location: audio\idirectmusicsynthsink_setmasterclock.htm
tech.root: dshow
ms.assetid: 91c996cc-04e1-47fb-a82d-1cb17fe191e2
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynthSink interface [Audio Devices],SetMasterClock method, IDirectMusicSynthSink.SetMasterClock, IDirectMusicSynthSink::SetMasterClock, SetMasterClock, SetMasterClock method [Audio Devices], SetMasterClock method [Audio Devices],IDirectMusicSynthSink interface, audio.idirectmusicsynthsink_setmasterclock, audmp-routines_45d219a0-1877-4a19-961f-6f3666bc9a1a.xml, dmusics/IDirectMusicSynthSink::SetMasterClock
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
 - IDirectMusicSynthSink::SetMasterClock
 - dmusics/IDirectMusicSynthSink::SetMasterClock
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
 - IDirectMusicSynthSink.SetMasterClock
archived: true
---

# IDirectMusicSynthSink::SetMasterClock


## -description

The <code>SetMasterClock</code> method provides the synth sink with a master time source, which is required for synchronization with the rest of DirectMusic.

## -parameters

### -param pClock

Specifies the master clock to synchronize to. This parameter is a pointer to the master-clock object's <b>IReferenceClock</b> interface (described in the Microsoft Windows SDK documentation).

## -returns

<code>SetMasterClock</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is unable to accept clock.

</td>
</tr>
</table>

## -remarks

The synth sink cannot function until it has received a master clock to synchronize the streaming wave with the rest of DirectMusic.

Because the master time and sample time might be driven by different crystals, they can drift apart. The synth sink can lock its understanding of the current sample time to the master time with a phase-locked loop.

The master clock is different from the latency clock, which is retrieved from the synth sink with a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getlatencyclock">IDirectMusicSynth::GetLatencyClock</a>. While the master clock provides the time base, the latency clock simply tracks the progress of the rendering of notes into the wave stream. This enables the application to know the earliest time it can submit a message for playback by using the <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-playbuffer">IDirectMusicSynth::PlayBuffer</a> method. The latency clock should be tightly synchronized to the master clock, so its units are relative.

You can measure the latency of the synthesizer by comparing the time of the latency clock with that of the master clock. Note that the latency clock will have jitter, reflecting the bursty nature of synthesizer mixing (each call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-render">IDirectMusicSynth::Render</a> jumps forward by the buffer length). In contrast, the master clock increments smoothly.

The <i>pClock</i> parameter follows the <a href="/windows-hardware/drivers/audio/reference-counting-conventions-for-com-objects">reference-counting conventions for COM objects</a>.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getlatencyclock">IDirectMusicSynth::GetLatencyClock</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-playbuffer">IDirectMusicSynth::PlayBuffer</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-render">IDirectMusicSynth::Render</a>