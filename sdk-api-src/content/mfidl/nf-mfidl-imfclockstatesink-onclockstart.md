---
UID: NF:mfidl.IMFClockStateSink.OnClockStart
title: IMFClockStateSink::OnClockStart (mfidl.h)
description: Called when the presentation clock starts.
helpviewer_keywords: ["1a696ffc-b8e6-4ef9-b980-35bfbd3d4128","IMFClockStateSink interface [Media Foundation]","OnClockStart method","IMFClockStateSink.OnClockStart","IMFClockStateSink::OnClockStart","OnClockStart","OnClockStart method [Media Foundation]","OnClockStart method [Media Foundation]","IMFClockStateSink interface","mf.imfclockstatesink_onclockstart","mfidl/IMFClockStateSink::OnClockStart"]
old-location: mf\imfclockstatesink_onclockstart.htm
tech.root: mf
ms.assetid: 1a696ffc-b8e6-4ef9-b980-35bfbd3d4128
ms.date: 12/05/2018
ms.keywords: 1a696ffc-b8e6-4ef9-b980-35bfbd3d4128, IMFClockStateSink interface [Media Foundation],OnClockStart method, IMFClockStateSink.OnClockStart, IMFClockStateSink::OnClockStart, OnClockStart, OnClockStart method [Media Foundation], OnClockStart method [Media Foundation],IMFClockStateSink interface, mf.imfclockstatesink_onclockstart, mfidl/IMFClockStateSink::OnClockStart
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFClockStateSink::OnClockStart
 - mfidl/IMFClockStateSink::OnClockStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFClockStateSink.OnClockStart
---

# IMFClockStateSink::OnClockStart


## -description

Called when the presentation clock starts.

## -parameters

### -param hnsSystemTime [in]

The system time when the clock started, in 100-nanosecond units.

### -param llClockStartOffset [in]

The new starting time for the clock, in 100-nanosecond units. This parameter can also equal <b>PRESENTATION_CURRENT_POSITION</b>, indicating the clock has started or restarted from its current position.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called when the presentation clock's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start">IMFPresentationClock::Start</a> method is called, with the following exception: If the clock is paused and <b>Start</b> is called with the value <b>PRESENTATION_CURRENT_POSITION</b>, <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart">IMFClockStateSink::OnClockRestart</a> is called instead of <b>OnClockStart</b>.

The clock notifies the presentation time source by calling the time source's <b>OnClockStart</b> method. This call occurs synchronously within the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start">Start</a> method. If the time source returns an error from <b>OnClockStart</b>, the presentation clock's <b>Start</b> method returns an error and the state change does not take place.

For any object that is not the presentation time source, the <b>OnClockStart</b> method is called asynchronously, after the state change is completed. In that case, the return value from this method is ignored.

The value given in <i>llClockStartOffset</i> is the presentation time when the clock starts, so it is relative to the start of the presentation. Media sinks should not render any data with a presentation time earlier than <i>llClockStartOffSet</i>. If a sample straddles the offset—that is, if the offset falls between the sample's start and stop times—the sink should either trim the sample so that only data after <i>llClockStartOffset</i> is rendered, or else simply drop the sample.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>