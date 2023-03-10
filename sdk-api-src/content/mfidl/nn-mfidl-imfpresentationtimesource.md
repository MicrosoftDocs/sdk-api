---
UID: NN:mfidl.IMFPresentationTimeSource
title: IMFPresentationTimeSource (mfidl.h)
description: Provides the clock times for the presentation clock.
helpviewer_keywords: ["IMFPresentationTimeSource","IMFPresentationTimeSource interface [Media Foundation]","IMFPresentationTimeSource interface [Media Foundation]","described","e5fab6b7-0abc-4ad7-89a9-33c673e97ce2","mf.imfpresentationtimesource","mfidl/IMFPresentationTimeSource"]
old-location: mf\imfpresentationtimesource.htm
tech.root: mf
ms.assetid: e5fab6b7-0abc-4ad7-89a9-33c673e97ce2
ms.date: 12/05/2018
ms.keywords: IMFPresentationTimeSource, IMFPresentationTimeSource interface [Media Foundation], IMFPresentationTimeSource interface [Media Foundation],described, e5fab6b7-0abc-4ad7-89a9-33c673e97ce2, mf.imfpresentationtimesource, mfidl/IMFPresentationTimeSource
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
 - IMFPresentationTimeSource
 - mfidl/IMFPresentationTimeSource
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
 - IMFPresentationTimeSource
---

# IMFPresentationTimeSource interface


## -description

Provides the clock times for the presentation clock.

## -inheritance

The <b>IMFPresentationTimeSource</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>. <b>IMFPresentationTimeSource</b> also has these types of members:

## -remarks

This interface is implemented by presentation time sources. A presentation time source is an object that provides the clock time for the presentation clock. For example, the audio renderer is a presentation time source. The rate at which the audio renderer consumes audio samples determines the clock time. If the audio format is 44100 samples per second, the audio renderer will report that one second has passed for every 44100 audio samples it plays. In this case, the timing is provided by the sound card.

To set the presentation time source on the presentation clock, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource">IMFPresentationClock::SetTimeSource</a> with a pointer to the time source's <b>IMFPresentationTimeSource</b> interface.

A presentation time source must also implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a> interface. The presentation clock uses this interface to notify the time source when the clock state changes.

Media Foundation provides a presentation time source that is based on the system clock. To create this object, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource">MFCreateSystemTimeSource</a> function.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
