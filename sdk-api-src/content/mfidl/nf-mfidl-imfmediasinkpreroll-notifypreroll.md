---
UID: NF:mfidl.IMFMediaSinkPreroll.NotifyPreroll
title: IMFMediaSinkPreroll::NotifyPreroll (mfidl.h)
description: Notifies the media sink that the presentation clock is about to start.
helpviewer_keywords: ["IMFMediaSinkPreroll interface [Media Foundation]","NotifyPreroll method","IMFMediaSinkPreroll.NotifyPreroll","IMFMediaSinkPreroll::NotifyPreroll","NotifyPreroll","NotifyPreroll method [Media Foundation]","NotifyPreroll method [Media Foundation]","IMFMediaSinkPreroll interface","d0694ad9-a18a-4fea-a9ff-b416bd4827ba","mf.imfmediasinkpreroll_notifypreroll","mfidl/IMFMediaSinkPreroll::NotifyPreroll"]
old-location: mf\imfmediasinkpreroll_notifypreroll.htm
tech.root: mf
ms.assetid: d0694ad9-a18a-4fea-a9ff-b416bd4827ba
ms.date: 12/05/2018
ms.keywords: IMFMediaSinkPreroll interface [Media Foundation],NotifyPreroll method, IMFMediaSinkPreroll.NotifyPreroll, IMFMediaSinkPreroll::NotifyPreroll, NotifyPreroll, NotifyPreroll method [Media Foundation], NotifyPreroll method [Media Foundation],IMFMediaSinkPreroll interface, d0694ad9-a18a-4fea-a9ff-b416bd4827ba, mf.imfmediasinkpreroll_notifypreroll, mfidl/IMFMediaSinkPreroll::NotifyPreroll
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
 - IMFMediaSinkPreroll::NotifyPreroll
 - mfidl/IMFMediaSinkPreroll::NotifyPreroll
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
 - IMFMediaSinkPreroll.NotifyPreroll
---

# IMFMediaSinkPreroll::NotifyPreroll


## -description

Notifies the media sink that the presentation clock is about to start.

## -parameters

### -param hnsUpcomingStartTime [in]

The upcoming start time for the presentation clock, in 100-nanosecond units. This time is the same value that will be given to the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start">IMFPresentationClock::Start</a> method when the presentation clock is started.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After this method is called, the media sink sends any number of <a href="/windows/desktop/medfound/mestreamsinkrequestsample">MEStreamSinkRequestSample</a> events to request samples, until is has enough preroll data. When it has enough preroll data, the media sink sends an <a href="/windows/desktop/medfound/mestreamsinkprerolled">MEStreamSinkPrerolled</a> event. This event signals that the client can start the presentation clock.
      

During preroll, the media sink can prepare the samples that it receives, so that they are ready to be rendered. It does not actually render any samples until the clock starts.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll">IMFMediaSinkPreroll</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>