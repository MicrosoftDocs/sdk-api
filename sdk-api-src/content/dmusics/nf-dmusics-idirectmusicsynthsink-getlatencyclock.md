---
UID: NF:dmusics.IDirectMusicSynthSink.GetLatencyClock
title: IDirectMusicSynthSink::GetLatencyClock (dmusics.h)
description: The GetLatencyClock method retrieves the latency clock, which measures the progress of the output audio stream.
helpviewer_keywords: ["GetLatencyClock","GetLatencyClock method [Audio Devices]","GetLatencyClock method [Audio Devices]","IDirectMusicSynthSink interface","IDirectMusicSynthSink interface [Audio Devices]","GetLatencyClock method","IDirectMusicSynthSink.GetLatencyClock","IDirectMusicSynthSink::GetLatencyClock","audio.idirectmusicsynthsink_getlatencyclock","audmp-routines_13de73b3-d0c6-4693-a56c-919628c63efb.xml","dmusics/IDirectMusicSynthSink::GetLatencyClock"]
old-location: audio\idirectmusicsynthsink_getlatencyclock.htm
tech.root: dshow
ms.assetid: 6f767ef2-6f7e-49b7-a169-09db49f55622
ms.date: 12/05/2018
ms.keywords: GetLatencyClock, GetLatencyClock method [Audio Devices], GetLatencyClock method [Audio Devices],IDirectMusicSynthSink interface, IDirectMusicSynthSink interface [Audio Devices],GetLatencyClock method, IDirectMusicSynthSink.GetLatencyClock, IDirectMusicSynthSink::GetLatencyClock, audio.idirectmusicsynthsink_getlatencyclock, audmp-routines_13de73b3-d0c6-4693-a56c-919628c63efb.xml, dmusics/IDirectMusicSynthSink::GetLatencyClock
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
 - IDirectMusicSynthSink::GetLatencyClock
 - dmusics/IDirectMusicSynthSink::GetLatencyClock
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
 - IDirectMusicSynthSink.GetLatencyClock
archived: true
---

# IDirectMusicSynthSink::GetLatencyClock


## -description

The <code>GetLatencyClock</code> method retrieves the latency clock, which measures the progress of the output audio stream.

## -parameters

### -param ppClock

Output pointer for the latency clock. This parameter points to a caller-allocated pointer variable into which the method writes a pointer to the latency-clock object's <b>IReferenceClock</b> interface (described in the Microsoft Windows SDK documentation).

## -returns

<code>GetLatencyClock</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates that the method is unable to access latency clock.

</td>
</tr>
</table>

## -remarks

The latency <b>IReferenceClock</b> returns the current render time whenever its <b>IReferenceClock::GetTime</b> method is called. This time is always relative to the time established by the master clock, installed in the synth sink by using <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-setmasterclock">IDirectMusicSynthSink::SetMasterClock</a>. The latency time is used by the performance layer of DirectMusic to identify the next available time to start playing a note.

The <i>ppClock</i> parameter follows the <a href="/windows-hardware/drivers/audio/reference-counting-conventions-for-com-objects">reference-counting conventions for COM objects</a>.

For more information about latency clocks, see <a href="/windows-hardware/drivers/audio/synthesizer-latency">Synthesizer Latency</a>. Also see the descriptions of the <b>IReferenceClock</b> and <b>IDirectMusic</b> interfaces in the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynth">IDirectMusicSynth</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setmasterclock">IDirectMusicSynth::SetMasterClock</a>