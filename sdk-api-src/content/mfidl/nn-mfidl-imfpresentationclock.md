---
UID: NN:mfidl.IMFPresentationClock
title: IMFPresentationClock (mfidl.h)
description: Represents a presentation clock, which is used to schedule when samples are rendered and to synchronize multiple streams.
helpviewer_keywords: ["979c4f77-cbee-468c-8f6b-e68442d89025","IMFPresentationClock","IMFPresentationClock interface [Media Foundation]","IMFPresentationClock interface [Media Foundation]","described","mf.imfpresentationclock","mfidl/IMFPresentationClock"]
old-location: mf\imfpresentationclock.htm
tech.root: mf
ms.assetid: 979c4f77-cbee-468c-8f6b-e68442d89025
ms.date: 12/05/2018
ms.keywords: 979c4f77-cbee-468c-8f6b-e68442d89025, IMFPresentationClock, IMFPresentationClock interface [Media Foundation], IMFPresentationClock interface [Media Foundation],described, mf.imfpresentationclock, mfidl/IMFPresentationClock
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
 - IMFPresentationClock
 - mfidl/IMFPresentationClock
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
 - IMFPresentationClock
---

# IMFPresentationClock interface


## -description

Represents a presentation clock, which is used to schedule when samples are rendered and to synchronize multiple streams.

## -inheritance

The <b>IMFPresentationClock</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>. <b>IMFPresentationClock</b> also has these types of members:

## -remarks

To create a new instance of the presentation clock, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock">MFCreatePresentationClock</a> function. The presentation clock must have a time source, which is an object that provides the clock times. For example, the audio renderer is a time source that uses the sound card to drive the clock. Time sources expose the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource">IMFPresentationTimeSource</a> interface. To set the time source, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource">SetTimeSource</a>. The presentation clock does not begin running until the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start">Start</a> method is called.

To get the presentation clock from the Media Session, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock">IMFMediaSession::GetClock</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
