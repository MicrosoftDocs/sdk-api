---
UID: NF:dmusics.IDirectMusicSynth.SetMasterClock
title: IDirectMusicSynth::SetMasterClock (dmusics.h)
description: The SetMasterClock method provides the synthesizer with a master time source, which the synthesizer requires to synchronize itself with the rest of DirectMusic.
helpviewer_keywords: ["IDirectMusicSynth interface [Audio Devices]","SetMasterClock method","IDirectMusicSynth.SetMasterClock","IDirectMusicSynth::SetMasterClock","SetMasterClock","SetMasterClock method [Audio Devices]","SetMasterClock method [Audio Devices]","IDirectMusicSynth interface","audio.idirectmusicsynth_setmasterclock","audmp-routines_4e91a462-de4e-4aed-bd0d-7ba1e91ccb36.xml","dmusics/IDirectMusicSynth::SetMasterClock"]
old-location: audio\idirectmusicsynth_setmasterclock.htm
tech.root: dshow
ms.assetid: 1585cfcc-2c83-4705-b465-52a621ccc163
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],SetMasterClock method, IDirectMusicSynth.SetMasterClock, IDirectMusicSynth::SetMasterClock, SetMasterClock, SetMasterClock method [Audio Devices], SetMasterClock method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_setmasterclock, audmp-routines_4e91a462-de4e-4aed-bd0d-7ba1e91ccb36.xml, dmusics/IDirectMusicSynth::SetMasterClock
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
 - IDirectMusicSynth::SetMasterClock
 - dmusics/IDirectMusicSynth::SetMasterClock
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
 - IDirectMusicSynth.SetMasterClock
archived: true
---

# IDirectMusicSynth::SetMasterClock


## -description

The <code>SetMasterClock</code> method provides the synthesizer with a master time source, which the synthesizer requires to synchronize itself with the rest of DirectMusic.

## -parameters

### -param pClock

Pointer to the master <b>IReferenceClock</b> (defined in Microsoft Windows SDK documentation) object, which is used by all devices in the current instance of DirectMusic.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Indicates a bad interface pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not open or not properly configured.

</td>
</tr>
</table>

## -remarks

The synthesizer wave-output device, which is managed by <a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a>, cannot function until it has received a master clock to synchronize to. It phase locks its own internal clock to the master clock, and is thus able to provide timing information to the synthesizer so it can make sense of the time stamps it receives in the calls to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-playbuffer">IDirectMusicSynth::PlayBuffer</a>.

In most implementations, <code>SetMasterClock</code> does little more than pass the master clock to the <b>IDirectMusicSynthSink</b> with a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-setmasterclock">IDirectMusicSynthSink::SetMasterClock</a>.

The master clock is very different from the latency clock, which is retrieved from the synth with a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getlatencyclock">IDirectMusicSynth::GetLatencyClock</a>. While the master clock provides the time base, the latency clock simply tracks the progress of the synthesizer's render engine. This enables the application to know the earliest time that it can submit an event for playback by calling the <b>PlayBuffer</b> method. The latency clock is tightly synchronized to the master clock, so its units are relative.

You can measure the latency of the synthesizer by comparing the time of the latency clock with the master clock. Note that the latency clock will have jitter, reflecting the bursts of synthesizer mixing, while the master clock should increment smoothly. Latency should not exceed 450 milliseconds.

For more information, see the description of the <b>IDirectMusic</b> interface in the Windows SDK documentation.

The <i>pClock</i> parameter follows the <a href="/windows-hardware/drivers/audio/reference-counting-conventions-for-com-objects">reference-counting conventions for COM objects</a>.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getlatencyclock">IDirectMusicSynth::GetLatencyClock</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-playbuffer">IDirectMusicSynth::PlayBuffer</a>



<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-setmasterclock">IDirectMusicSynthSink::SetMasterClock</a>