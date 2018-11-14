---
UID: NF:segment.IMSVidTunerEvent.TuneChanged
title: IMSVidTunerEvent::TuneChanged
author: windows-sdk-content
description: This topic applies to Windows XP or later.
old-location: mstv\imsvidtunerevent_tunechanged.htm
tech.root: MSTV
ms.assetid: 5fc30a5a-b934-4c75-9cc8-5a039843ebe8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidTunerEvent interface [Microsoft TV Technologies],TuneChanged method, IMSVidTunerEvent.TuneChanged, IMSVidTunerEvent::TuneChanged, IMSVidTunerEventTuneChanged, TuneChanged, TuneChanged method [Microsoft TV Technologies], TuneChanged method [Microsoft TV Technologies],IMSVidTunerEvent interface, mstv.imsvidtunerevent_tunechanged, segment/IMSVidTunerEvent::TuneChanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidTunerEvent.TuneChanged
: 
---

# IMSVidTunerEvent::TuneChanged


## -description



This topic applies to Windows XP or later.
        



The <b>TuneChanged</b> method signals that the tuner has tuned to a new frequency.


## -parameters




### -param lpd

TBD




#### - plpd [in]

Pointer to the <b>MSVidTuner</b> object that fired the event.


## -returns



Return S_OK or an error code.




## -remarks



The dispatch identifier (dispid) of this method is <b>eventidOnTuneChanged</b>.




## -see-also




<a href="https://msdn.microsoft.com/cdffe6ca-00b0-4230-963d-b4409413e5f5">IMSVidTunerEvent Interface</a>
 

 

