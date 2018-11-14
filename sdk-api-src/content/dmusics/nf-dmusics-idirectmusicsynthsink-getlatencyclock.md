---
UID: NF:dmusics.IDirectMusicSynthSink.GetLatencyClock
title: IDirectMusicSynthSink::GetLatencyClock
author: windows-sdk-content
description: The GetLatencyClock method retrieves the latency clock, which measures the progress of the output audio stream.
old-location: audio\idirectmusicsynthsink_getlatencyclock.htm
tech.root: audio
ms.assetid: 6f767ef2-6f7e-49b7-a169-09db49f55622
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetLatencyClock, GetLatencyClock method [Audio Devices], GetLatencyClock method [Audio Devices],IDirectMusicSynthSink interface, IDirectMusicSynthSink interface [Audio Devices],GetLatencyClock method, IDirectMusicSynthSink.GetLatencyClock, IDirectMusicSynthSink::GetLatencyClock, audio.idirectmusicsynthsink_getlatencyclock, audmp-routines_13de73b3-d0c6-4693-a56c-919628c63efb.xml, dmusics/IDirectMusicSynthSink::GetLatencyClock
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirectMusicSynthSink.GetLatencyClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dmusics.h
: 
- IDirectMusicSynthSink.GetLatencyClock
: 
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



The latency <b>IReferenceClock</b> returns the current render time whenever its <b>IReferenceClock::GetTime</b> method is called. This time is always relative to the time established by the master clock, installed in the synth sink by using <a href="https://msdn.microsoft.com/91c996cc-04e1-47fb-a82d-1cb17fe191e2">IDirectMusicSynthSink::SetMasterClock</a>. The latency time is used by the performance layer of DirectMusic to identify the next available time to start playing a note.

The <i>ppClock</i> parameter follows the <a href="https://msdn.microsoft.com/e6b19110-37e2-4d23-a528-6393c12ab650">reference-counting conventions for COM objects</a>.

For more information about latency clocks, see <a href="https://msdn.microsoft.com/a3134024-77b9-463b-959b-3c910f83014d">Synthesizer Latency</a>. Also see the descriptions of the <b>IReferenceClock</b> and <b>IDirectMusic</b> interfaces in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/08f1056a-fead-475b-a13a-ee11b9709241">IDirectMusicSynth</a>



<a href="https://msdn.microsoft.com/1585cfcc-2c83-4705-b465-52a621ccc163">IDirectMusicSynth::SetMasterClock</a>
 

 

