---
UID: NF:mfidl.IMFClockStateSink.OnClockRestart
title: IMFClockStateSink::OnClockRestart (mfidl.h)
description: Called when the presentation clock restarts from the same position while paused.
helpviewer_keywords: ["55973dfa-59b9-4105-9706-5d5497ad2818","IMFClockStateSink interface [Media Foundation]","OnClockRestart method","IMFClockStateSink.OnClockRestart","IMFClockStateSink::OnClockRestart","OnClockRestart","OnClockRestart method [Media Foundation]","OnClockRestart method [Media Foundation]","IMFClockStateSink interface","mf.imfclockstatesink_onclockrestart","mfidl/IMFClockStateSink::OnClockRestart"]
old-location: mf\imfclockstatesink_onclockrestart.htm
tech.root: mf
ms.assetid: 55973dfa-59b9-4105-9706-5d5497ad2818
ms.date: 12/05/2018
ms.keywords: 55973dfa-59b9-4105-9706-5d5497ad2818, IMFClockStateSink interface [Media Foundation],OnClockRestart method, IMFClockStateSink.OnClockRestart, IMFClockStateSink::OnClockRestart, OnClockRestart, OnClockRestart method [Media Foundation], OnClockRestart method [Media Foundation],IMFClockStateSink interface, mf.imfclockstatesink_onclockrestart, mfidl/IMFClockStateSink::OnClockRestart
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
 - IMFClockStateSink::OnClockRestart
 - mfidl/IMFClockStateSink::OnClockRestart
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
 - IMFClockStateSink.OnClockRestart
---

# IMFClockStateSink::OnClockRestart


## -description

Called when the presentation clock restarts from the same position while paused.

## -parameters

### -param hnsSystemTime [in]

The system time when the clock restarted, in 100-nanosecond units.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called if the presentation clock is paused and the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start">IMFPresentationClock::Start</a> method is called with the value <b>PRESENTATION_CURRENT_POSITION</b>.
      

The clock notifies the presentation time source by calling the time source's <b>OnClockRestart</b> method. This call occurs synchronously within the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start">Start</a> method. If the time source returns an error from <b>OnClockRestart</b>, the presentation clock's <b>Start</b> method returns an error and the state change does not take place.
      

For any object that is not the presentation time source, the <b>OnClockRestart</b> method is called asynchronously, after the state change is completed. In that case, the return value from this method is ignored.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>