---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

The master clock is different from the latency clock, which is retrieved from the synth sink with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536536">IDirectMusicSynth::GetLatencyClock</a>. While the master clock provides the time base, the latency clock simply tracks the progress of the rendering of notes into the wave stream. This enables the application to know the earliest time it can submit a message for playback by using the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536540">IDirectMusicSynth::PlayBuffer</a> method. The latency clock should be tightly synchronized to the master clock, so its units are relative.

You can measure the latency of the synthesizer by comparing the time of the latency clock with that of the master clock. Note that the latency clock will have jitter, reflecting the bursty nature of synthesizer mixing (each call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536541">IDirectMusicSynth::Render</a> jumps forward by the buffer length). In contrast, the master clock increments smoothly.

The <i>pClock</i> parameter follows the <a href="https://msdn.microsoft.com/e6b19110-37e2-4d23-a528-6393c12ab650">reference-counting conventions for COM objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536536">IDirectMusicSynth::GetLatencyClock</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536540">IDirectMusicSynth::PlayBuffer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536541">IDirectMusicSynth::Render</a>
 

 

