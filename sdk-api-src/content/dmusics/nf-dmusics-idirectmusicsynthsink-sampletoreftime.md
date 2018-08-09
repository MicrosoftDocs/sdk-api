---
UID: NF:dmusics.IDirectMusicSynthSink.SampleToRefTime
title: IDirectMusicSynthSink::SampleToRefTime
author: windows-sdk-content
description: The SampleToRefTime method converts a sample time to a reference time.
old-location: audio\idirectmusicsynthsink_sampletoreftime.htm
old-project: audio
ms.assetid: a82b33a3-e7bb-46f0-a13d-ba251db19c16
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDirectMusicSynthSink interface [Audio Devices],SampleToRefTime method, IDirectMusicSynthSink.SampleToRefTime, IDirectMusicSynthSink::SampleToRefTime, SampleToRefTime, SampleToRefTime method [Audio Devices], SampleToRefTime method [Audio Devices],IDirectMusicSynthSink interface, audio.idirectmusicsynthsink_sampletoreftime, audmp-routines_fc97fec3-8fa0-4f6a-82b5-b99c434341c4.xml, dmusics/IDirectMusicSynthSink::SampleToRefTime
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DMO_PARTIAL_MEDIATYPE, *PDMO_PARTIAL_MEDIATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusics.h
api_name:
 - IDirectMusicSynthSink.SampleToRefTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectMusicSynthSink::SampleToRefTime


## -description


The <code>SampleToRefTime</code> method converts a sample time to a reference time.


## -parameters




### -param llSampleTime

Specifies the sample time. For more information, see the following Remarks section.


### -param prfTime

Output pointer for the reference time. This parameter points to a caller-allocated REFERENCE_TIME variable into which the method writes the reference time.


## -returns



<code>SampleToRefTime</code> returns S_OK if the call is successful. Otherwise, the method returns an appropriate error code. 




## -remarks



The <code>SampleToRefTime</code> method converts sample time to reference time. Sample time is expressed as the number of samples rendered, and reference time is measured in 100-nanosecond units.

The synth sink manages the timing relationship between the master clock (set with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536528">IDirectMusicSynthSink::SetMasterClock</a>) and the audio stream.

For more information, see the description of reference time and sample time in <a href="https://msdn.microsoft.com/38aca8b7-f895-4b16-aaac-5a13973cf976">Synthesizer Timing</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536525">IDirectMusicSynthSink::RefTimeToSample</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536528">IDirectMusicSynthSink::SetMasterClock</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537018">ISynthSinkDMus::SampleToRefTime</a>
 

 

