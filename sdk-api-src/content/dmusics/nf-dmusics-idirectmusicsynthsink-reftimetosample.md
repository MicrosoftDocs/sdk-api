---
UID: NF:dmusics.IDirectMusicSynthSink.RefTimeToSample
title: IDirectMusicSynthSink::RefTimeToSample
author: windows-sdk-content
description: The RefTimeToSample method converts a reference time to a sample time.
old-location: audio\idirectmusicsynthsink_reftimetosample.htm
old-project: audio
ms.assetid: 11a6b670-93d6-4455-b279-a1fc5fca0d1d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDirectMusicSynthSink interface [Audio Devices],RefTimeToSample method, IDirectMusicSynthSink.RefTimeToSample, IDirectMusicSynthSink::RefTimeToSample, RefTimeToSample, RefTimeToSample method [Audio Devices], RefTimeToSample method [Audio Devices],IDirectMusicSynthSink interface, audio.idirectmusicsynthsink_reftimetosample, audmp-routines_0e3d6a54-9625-48de-8ac2-2359047acd90.xml, dmusics/IDirectMusicSynthSink::RefTimeToSample
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dmusics.h
req.include-header: Dmusics.h
req.redist: 
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
 - IDirectMusicSynthSink.RefTimeToSample
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectMusicSynthSink::RefTimeToSample


## -description


The <code>RefTimeToSample</code> method converts a reference time to a sample time.


## -parameters




### -param rfTime

Specifies the reference time. Reference time is measured in 100-nanosecond units.


### -param pllSampleTime

Output pointer for the sample time. This parameter points to a caller-allocated LONGLONG variable into which the method writes the sample time.


## -returns



<code>RefTimeToSample</code> returns S_OK if the call is successful. Otherwise, the method returns an appropriate error code.




## -remarks



The <code>RefTimeToSample</code> method converts reference time to sample time. The method accepts a reference time as an input parameter, and it outputs the corresponding sample time.

The calculation of sample time from reference time depends on the sampling frequency. For example, if the output buffer is in a 44.2 kHz format, a sample time of 44,200 is equivalent to a reference time of one second.

The synth sink manages the timing relationship between the master clock (set with a call to <a href="https://msdn.microsoft.com/91c996cc-04e1-47fb-a82d-1cb17fe191e2">IDirectMusicSynthSink::SetMasterClock</a>) and the audio stream.

For more information, see the description of reference time and sample time in <a href="https://msdn.microsoft.com/38aca8b7-f895-4b16-aaac-5a13973cf976">Synthesizer Timing</a>.




## -see-also




<a href="https://msdn.microsoft.com/a82b33a3-e7bb-46f0-a13d-ba251db19c16">IDirectMusicSynthSink::SampleToRefTime</a>



<a href="https://msdn.microsoft.com/91c996cc-04e1-47fb-a82d-1cb17fe191e2">IDirectMusicSynthSink::SetMasterClock</a>



<a href="https://msdn.microsoft.com/20906bcd-3059-4d10-92cb-8efdef929ccd">ISynthSinkDMus::RefTimeToSample</a>
 

 

