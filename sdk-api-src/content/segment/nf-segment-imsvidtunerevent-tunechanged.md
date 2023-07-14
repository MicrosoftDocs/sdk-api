---
UID: NF:segment.IMSVidTunerEvent.TuneChanged
title: IMSVidTunerEvent::TuneChanged (segment.h)
description: This topic applies to Windows XP or later.
helpviewer_keywords: ["IMSVidTunerEvent interface [Microsoft TV Technologies]","TuneChanged method","IMSVidTunerEvent.TuneChanged","IMSVidTunerEvent::TuneChanged","IMSVidTunerEventTuneChanged","TuneChanged","TuneChanged method [Microsoft TV Technologies]","TuneChanged method [Microsoft TV Technologies]","IMSVidTunerEvent interface","mstv.imsvidtunerevent_tunechanged","segment/IMSVidTunerEvent::TuneChanged"]
old-location: mstv\imsvidtunerevent_tunechanged.htm
tech.root: mstv
ms.assetid: 5fc30a5a-b934-4c75-9cc8-5a039843ebe8
ms.date: 12/05/2018
ms.keywords: IMSVidTunerEvent interface [Microsoft TV Technologies],TuneChanged method, IMSVidTunerEvent.TuneChanged, IMSVidTunerEvent::TuneChanged, IMSVidTunerEventTuneChanged, TuneChanged, TuneChanged method [Microsoft TV Technologies], TuneChanged method [Microsoft TV Technologies],IMSVidTunerEvent interface, mstv.imsvidtunerevent_tunechanged, segment/IMSVidTunerEvent::TuneChanged
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidTunerEvent::TuneChanged
 - segment/IMSVidTunerEvent::TuneChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidTunerEvent.TuneChanged
---

# IMSVidTunerEvent::TuneChanged


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP or later.
        



The <b>TuneChanged</b> method signals that the tuner has tuned to a new frequency.

## -parameters

### -param lpd [in]

Pointer to the <b>MSVidTuner</b> object that fired the event.

## -returns

Return S_OK or an error code.

## -remarks

The dispatch identifier (dispid) of this method is <b>eventidOnTuneChanged</b>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidtunerevent">IMSVidTunerEvent Interface</a>