---
UID: NF:mfidl.IMFClockStateSink.OnClockPause
title: IMFClockStateSink::OnClockPause (mfidl.h)
description: Called when the presentation clock pauses.
helpviewer_keywords: ["IMFClockStateSink interface [Media Foundation]","OnClockPause method","IMFClockStateSink.OnClockPause","IMFClockStateSink::OnClockPause","OnClockPause","OnClockPause method [Media Foundation]","OnClockPause method [Media Foundation]","IMFClockStateSink interface","d4eb1ddf-2eea-48e2-946a-4ea20be8cc8f","mf.imfclockstatesink_onclockpause","mfidl/IMFClockStateSink::OnClockPause"]
old-location: mf\imfclockstatesink_onclockpause.htm
tech.root: mf
ms.assetid: d4eb1ddf-2eea-48e2-946a-4ea20be8cc8f
ms.date: 12/05/2018
ms.keywords: IMFClockStateSink interface [Media Foundation],OnClockPause method, IMFClockStateSink.OnClockPause, IMFClockStateSink::OnClockPause, OnClockPause, OnClockPause method [Media Foundation], OnClockPause method [Media Foundation],IMFClockStateSink interface, d4eb1ddf-2eea-48e2-946a-4ea20be8cc8f, mf.imfclockstatesink_onclockpause, mfidl/IMFClockStateSink::OnClockPause
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
 - IMFClockStateSink::OnClockPause
 - mfidl/IMFClockStateSink::OnClockPause
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
 - IMFClockStateSink.OnClockPause
---

# IMFClockStateSink::OnClockPause


## -description

Called when the presentation clock pauses.

## -parameters

### -param hnsSystemTime [in]

The system time when the clock was paused, in 100-nanosecond units.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the presentation clock's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause">IMFPresentationClock::Pause</a> method is called, the clock notifies the presentation time source by calling the time source's <b>OnClockPause</b> method. This call occurs synchronously within the <b>Pause</b> method. If the time source returns an error from <b>OnClockPause</b>, the presentation clock's <b>Pause</b> method returns an error and the state change does not take place.

For any object that is not the presentation time source, the <b>OnClockPause</b> method is called asynchronously, after the state change is completed. In that case, the return value from this method is ignored.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>