---
UID: NF:dmusics.IDirectMusicSynth.GetLatencyClock
title: IDirectMusicSynth::GetLatencyClock (dmusics.h)
description: The GetLatencyClock method retrieves a reference to the IReferenceClock interface (described in the Microsoft Windows SDK documentation) of the reference-clock object that tracks the current mix time.
helpviewer_keywords: ["GetLatencyClock","GetLatencyClock method [Audio Devices]","GetLatencyClock method [Audio Devices]","IDirectMusicSynth interface","IDirectMusicSynth interface [Audio Devices]","GetLatencyClock method","IDirectMusicSynth.GetLatencyClock","IDirectMusicSynth::GetLatencyClock","audio.idirectmusicsynth_getlatencyclock","audmp-routines_79ca400b-e04b-4381-aacb-79a3f9415683.xml","dmusics/IDirectMusicSynth::GetLatencyClock"]
old-location: audio\idirectmusicsynth_getlatencyclock.htm
tech.root: dshow
ms.assetid: 36690d54-dc88-4e31-8f66-8a0b48be2712
ms.date: 12/05/2018
ms.keywords: GetLatencyClock, GetLatencyClock method [Audio Devices], GetLatencyClock method [Audio Devices],IDirectMusicSynth interface, IDirectMusicSynth interface [Audio Devices],GetLatencyClock method, IDirectMusicSynth.GetLatencyClock, IDirectMusicSynth::GetLatencyClock, audio.idirectmusicsynth_getlatencyclock, audmp-routines_79ca400b-e04b-4381-aacb-79a3f9415683.xml, dmusics/IDirectMusicSynth::GetLatencyClock
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
 - IDirectMusicSynth::GetLatencyClock
 - dmusics/IDirectMusicSynth::GetLatencyClock
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
 - IDirectMusicSynth.GetLatencyClock
archived: true
---

# IDirectMusicSynth::GetLatencyClock


## -description

The <code>GetLatencyClock</code> method retrieves a reference to the <b>IReferenceClock</b> interface (described in the Microsoft Windows SDK documentation) of the reference-clock object that tracks the current mix time.

## -parameters

### -param ppClock

Output pointer for the latency clock. This parameter points to a caller-allocated pointer variable into which the method writes a pointer to the latency-clock object's <b>IReferenceClock</b> interface. Through this interface, the synthesizer is able to get the current mix time. Specify a valid, non-NULL pointer value for this parameter.

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
Indicates that the method was unable to access the latency clock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <i>ppClock</i> pointer is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_NOSYNTHSINK</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>IDirectMusicSynthSink</b> object was not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not open or is not properly configured.

</td>
</tr>
</table>

## -remarks

This method returns the latency clock created by the wave sink (<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a>) object, which handles the output audio stream. The latency clock returns the current render time whenever its <b>IReferenceClock::GetTime</b> method is called. This time is always relative to the time established by the master clock (installed in the synthesizer and wave sink through a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setmasterclock">IDirectMusicSynth::SetMasterClock</a> and <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-setmasterclock">IDirectMusicSynthSink::SetMasterClock</a>). The latency time is used by the performance to identify the next available time to start playing a note. The latency should not exceed 450 milliseconds.

For more information about latency clocks, see <a href="/windows-hardware/drivers/audio/synthesizer-latency">Synthesizer Latency</a>. Also see the description of the <b>IDirectMusic</b> and <b>IReferenceClock</b> interfaces in the Windows SDK documentation.

The <i>ppClock</i> parameter follows the <a href="/windows-hardware/drivers/audio/reference-counting-conventions-for-com-objects">reference-counting conventions for COM objects</a>.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setmasterclock">IDirectMusicSynth::SetMasterClock</a>



<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-setmasterclock">IDirectMusicSynthSink::SetMasterClock</a>