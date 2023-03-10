---
UID: NN:mfidl.IMFClockStateSink
title: IMFClockStateSink (mfidl.h)
description: Receives state-change notifications from the presentation clock.
helpviewer_keywords: ["9aa0d2cd-a687-4b3a-834d-ccc8d3a03196","IMFClockStateSink","IMFClockStateSink interface [Media Foundation]","IMFClockStateSink interface [Media Foundation]","described","mf.imfclockstatesink","mfidl/IMFClockStateSink"]
old-location: mf\imfclockstatesink.htm
tech.root: mf
ms.assetid: 9aa0d2cd-a687-4b3a-834d-ccc8d3a03196
ms.date: 12/05/2018
ms.keywords: 9aa0d2cd-a687-4b3a-834d-ccc8d3a03196, IMFClockStateSink, IMFClockStateSink interface [Media Foundation], IMFClockStateSink interface [Media Foundation],described, mf.imfclockstatesink, mfidl/IMFClockStateSink
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
 - IMFClockStateSink
 - mfidl/IMFClockStateSink
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
 - IMFClockStateSink
---

# IMFClockStateSink interface


## -description

Receives state-change notifications from the presentation clock.

## -inheritance

The <b>IMFClockStateSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFClockStateSink</b> also has these types of members:

## -remarks

To receive state-change notifications from the presentation clock, implement this interface and call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink">IMFPresentationClock::AddClockStateSink</a> on the presentation clock.

This interface must be implemented by:

<ul>
<li>
Presentation time sources. The presentation clock uses this interface to request change states from the time source.

</li>
<li>
Media sinks. Media sinks use this interface to get notifications when the presentation clock changes.

</li>
</ul>
Other objects that need to be notified can implement this interface.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource">IMFPresentationTimeSource</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
