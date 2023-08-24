---
UID: NF:dmusics.IDirectMusicSynthSink.SampleToRefTime
title: IDirectMusicSynthSink::SampleToRefTime (dmusics.h)
description: The SampleToRefTime method converts a sample time to a reference time.
helpviewer_keywords: ["IDirectMusicSynthSink interface [Audio Devices]","SampleToRefTime method","IDirectMusicSynthSink.SampleToRefTime","IDirectMusicSynthSink::SampleToRefTime","SampleToRefTime","SampleToRefTime method [Audio Devices]","SampleToRefTime method [Audio Devices]","IDirectMusicSynthSink interface","audio.idirectmusicsynthsink_sampletoreftime","audmp-routines_fc97fec3-8fa0-4f6a-82b5-b99c434341c4.xml","dmusics/IDirectMusicSynthSink::SampleToRefTime"]
old-location: audio\idirectmusicsynthsink_sampletoreftime.htm
tech.root: dshow
ms.assetid: a82b33a3-e7bb-46f0-a13d-ba251db19c16
ms.date: 12/05/2018
ms.keywords: IDirectMusicSynthSink interface [Audio Devices],SampleToRefTime method, IDirectMusicSynthSink.SampleToRefTime, IDirectMusicSynthSink::SampleToRefTime, SampleToRefTime, SampleToRefTime method [Audio Devices], SampleToRefTime method [Audio Devices],IDirectMusicSynthSink interface, audio.idirectmusicsynthsink_sampletoreftime, audmp-routines_fc97fec3-8fa0-4f6a-82b5-b99c434341c4.xml, dmusics/IDirectMusicSynthSink::SampleToRefTime
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
 - IDirectMusicSynthSink::SampleToRefTime
 - dmusics/IDirectMusicSynthSink::SampleToRefTime
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
 - IDirectMusicSynthSink.SampleToRefTime
archived: true
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

The synth sink manages the timing relationship between the master clock (set with a call to <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-setmasterclock">IDirectMusicSynthSink::SetMasterClock</a>) and the audio stream.

For more information, see the description of reference time and sample time in <a href="/windows-hardware/drivers/audio/synthesizer-timing">Synthesizer Timing</a>.

## -see-also

<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-reftimetosample">IDirectMusicSynthSink::RefTimeToSample</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynthsink-setmasterclock">IDirectMusicSynthSink::SetMasterClock</a>



<a href="/windows-hardware/drivers/ddi/content/dmusicks/nf-dmusicks-isynthsinkdmus-sampletoreftime">ISynthSinkDMus::SampleToRefTime</a>