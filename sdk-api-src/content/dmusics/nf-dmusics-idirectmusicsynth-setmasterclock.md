---
UID: NF:dmusics.IDirectMusicSynth.SetMasterClock
title: IDirectMusicSynth::SetMasterClock (dmusics.h)
author: windows-sdk-content
description: The SetMasterClock method provides the synthesizer with a master time source, which the synthesizer requires to synchronize itself with the rest of DirectMusic.
old-location: audio\idirectmusicsynth_setmasterclock.htm
tech.root: audio
ms.assetid: 1585cfcc-2c83-4705-b465-52a621ccc163
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectMusicSynth interface [Audio Devices],SetMasterClock method, IDirectMusicSynth.SetMasterClock, IDirectMusicSynth::SetMasterClock, SetMasterClock, SetMasterClock method [Audio Devices], SetMasterClock method [Audio Devices],IDirectMusicSynth interface, audio.idirectmusicsynth_setmasterclock, audmp-routines_4e91a462-de4e-4aed-bd0d-7ba1e91ccb36.xml, dmusics/IDirectMusicSynth::SetMasterClock
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusics.h
api_name:
 - IDirectMusicSynth.SetMasterClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



The synthesizer wave-output device, which is managed by <a href="https://msdn.microsoft.com/11944933-cd95-4979-82b2-2c3875b221b3">IDirectMusicSynthSink</a>, cannot function until it has received a master clock to synchronize to. It phase locks its own internal clock to the master clock, and is thus able to provide timing information to the synthesizer so it can make sense of the time stamps it receives in the calls to <a href="https://msdn.microsoft.com/96d0a2ef-1265-4e04-bb70-920f4c82058c">IDirectMusicSynth::PlayBuffer</a>.

In most implementations, <code>SetMasterClock</code> does little more than pass the master clock to the <b>IDirectMusicSynthSink</b> with a call to <a href="https://msdn.microsoft.com/91c996cc-04e1-47fb-a82d-1cb17fe191e2">IDirectMusicSynthSink::SetMasterClock</a>.

The master clock is very different from the latency clock, which is retrieved from the synth with a call to <a href="https://msdn.microsoft.com/36690d54-dc88-4e31-8f66-8a0b48be2712">IDirectMusicSynth::GetLatencyClock</a>. While the master clock provides the time base, the latency clock simply tracks the progress of the synthesizer's render engine. This enables the application to know the earliest time that it can submit an event for playback by calling the <b>PlayBuffer</b> method. The latency clock is tightly synchronized to the master clock, so its units are relative.

You can measure the latency of the synthesizer by comparing the time of the latency clock with the master clock. Note that the latency clock will have jitter, reflecting the bursts of synthesizer mixing, while the master clock should increment smoothly. Latency should not exceed 450 milliseconds.

For more information, see the description of the <b>IDirectMusic</b> interface in the Windows SDK documentation.

The <i>pClock</i> parameter follows the <a href="https://msdn.microsoft.com/e6b19110-37e2-4d23-a528-6393c12ab650">reference-counting conventions for COM objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/36690d54-dc88-4e31-8f66-8a0b48be2712">IDirectMusicSynth::GetLatencyClock</a>



<a href="https://msdn.microsoft.com/96d0a2ef-1265-4e04-bb70-920f4c82058c">IDirectMusicSynth::PlayBuffer</a>



<a href="https://msdn.microsoft.com/11944933-cd95-4979-82b2-2c3875b221b3">IDirectMusicSynthSink</a>



<a href="https://msdn.microsoft.com/91c996cc-04e1-47fb-a82d-1cb17fe191e2">IDirectMusicSynthSink::SetMasterClock</a>
 

 

