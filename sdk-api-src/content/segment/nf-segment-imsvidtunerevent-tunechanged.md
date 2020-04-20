---
UID: NF:segment.IMSVidTunerEvent.TuneChanged
title: IMSVidTunerEvent::TuneChanged (segment.h)
description: This topic applies to Windows XP or later.helpviewer_keywords: ["IMSVidTunerEvent interface [Microsoft TV Technologies]","TuneChanged method","IMSVidTunerEvent.TuneChanged","IMSVidTunerEvent::TuneChanged","IMSVidTunerEventTuneChanged","TuneChanged","TuneChanged method [Microsoft TV Technologies]","TuneChanged method [Microsoft TV Technologies]","IMSVidTunerEvent interface","mstv.imsvidtunerevent_tunechanged","segment/IMSVidTunerEvent::TuneChanged"]
old-location: mstv\imsvidtunerevent_tunechanged.htm
tech.root: mstv
ms.assetid: 5fc30a5a-b934-4c75-9cc8-5a039843ebe8
ms.date: 12/05/2018
ms.keywords: IMSVidTunerEvent interface [Microsoft TV Technologies],TuneChanged method, IMSVidTunerEvent.TuneChanged, IMSVidTunerEvent::TuneChanged, IMSVidTunerEventTuneChanged, TuneChanged, TuneChanged method [Microsoft TV Technologies], TuneChanged method [Microsoft TV Technologies],IMSVidTunerEvent interface, mstv.imsvidtunerevent_tunechanged, segment/IMSVidTunerEvent::TuneChanged
f1_keywords:
- segment/IMSVidTunerEvent.TuneChanged
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidTunerEvent.TuneChanged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidTunerEvent::TuneChanged


## -description



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




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidtunerevent">IMSVidTunerEvent Interface</a>
 

 

