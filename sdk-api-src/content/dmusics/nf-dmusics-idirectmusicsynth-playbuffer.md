---
UID: NF:dmusics.IDirectMusicSynth.PlayBuffer
title: IDirectMusicSynth::PlayBuffer (dmusics.h)
description: The PlayBuffer method downloads a stream of MIDI messages to the synthesizer.
helpviewer_keywords: ["IDirectMusicSynth interface [Audio Devices]","PlayBuffer method","IDirectMusicSynth.PlayBuffer","IDirectMusicSynth::PlayBuffer","PlayBuffer","PlayBuffer method [Audio Devices]","PlayBuffer method [Audio Devices]","IDirectMusicSynth interface","audio.idirectmusicsynth_playbuffer","audmp-routines_1a5efe25-ef92-4baf-a4bc-fc2d043c832f.xml","dmusics/IDirectMusicSynth::PlayBuffer"]
old-location: audio\idirectmusicsynth_playbuffer.htm
tech.root: dshow
ms.assetid: 96d0a2ef-1265-4e04-bb70-920f4c82058c
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],PlayBuffer method, IDirectMusicSynth.PlayBuffer, IDirectMusicSynth::PlayBuffer, PlayBuffer, PlayBuffer method [Audio Devices], PlayBuffer method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_playbuffer, audmp-routines_1a5efe25-ef92-4baf-a4bc-fc2d043c832f.xml, dmusics/IDirectMusicSynth::PlayBuffer
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
 - IDirectMusicSynth::PlayBuffer
 - dmusics/IDirectMusicSynth::PlayBuffer
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
 - IDirectMusicSynth.PlayBuffer
archived: true
---

# IDirectMusicSynth::PlayBuffer


## -description

The <code>PlayBuffer</code> method downloads a stream of MIDI messages to the synthesizer.

## -parameters

### -param rt

Specifies the start time of the buffer. This value is specified in REFERENCE_TIME units, relative to the master clock, which was previously set with a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setmasterclock">IDirectMusicSynth::SetMasterClock</a>. Also, this value should be after the time returned by the clock in <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getlatencyclock">IDirectMusicSynth::GetLatencyClock</a>.

### -param pbBuffer

Pointer to a memory buffer containing the time-stamped MIDI messages that the <b>IDirectMusicBuffer</b> object generates

### -param cbBuffer

Specifies the size of the buffer in bytes.

## -returns

<code>PlayBuffer</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates a bad buffer pointer.

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
<dt><b>DMUS_E_SYNTHINACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method was called when the synth is inactive, which is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is unable to queue the messages.

</td>
</tr>
</table>

## -remarks

This is the software synthesizer's implementation of the <b>IDirectMusicPort::PlayBuffer</b> method. For details on the buffer format, see the description of <b>IDirectMusicPort::PlayBuffer</b> in the Microsoft Windows SDK documentation.

In order to properly associate the time stamp of each MIDI message in the buffer, the synth needs to convert from the REFERENCE_TIME format to its internal sample-based time. Because the wave-output stream is actually managed by <a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a>, the synth calls <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-reftimetosample">IDirectMusicSynthSink::RefTimeToSample</a> for each MIDI message to convert its time stamp into sample time.

Typically, the synthesizer pulls each MIDI message from the buffer, stamps it in sample time, and places it in its own internal queue. The queue is emptied later by the rendering process, which is managed by <b>IDirectMusicPort::Render</b> and called by the <b>IDirectMusicSynthSink</b> object.

For more information, see the descriptions of the <b>IDirectMusic</b>, <b>IDirectMusicPort</b>, and <b>IDirectMusicBuffer</b> interfaces in the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-getlatencyclock">IDirectMusicSynth::GetLatencyClock</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-render">IDirectMusicSynth::Render</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-setmasterclock">IDirectMusicSynth::SetMasterClock</a>



<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynthsink">IDirectMusicSynthSink</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-reftimetosample">IDirectMusicSynthSink::RefTimeToSample</a>