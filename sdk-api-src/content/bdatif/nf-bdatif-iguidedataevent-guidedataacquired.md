---
UID: NF:bdatif.IGuideDataEvent.GuideDataAcquired
title: IGuideDataEvent::GuideDataAcquired (bdatif.h)
description: The GuideDataAcquired method is called when a complete set of guide data has been acquired from the current transport stream.
helpviewer_keywords: ["GuideDataAcquired","GuideDataAcquired method [Microsoft TV Technologies]","GuideDataAcquired method [Microsoft TV Technologies]","IGuideDataEvent interface","IGuideDataEvent interface [Microsoft TV Technologies]","GuideDataAcquired method","IGuideDataEvent.GuideDataAcquired","IGuideDataEvent::GuideDataAcquired","IGuideDataEventGuideDataAcquired","bdatif/IGuideDataEvent::GuideDataAcquired","mstv.iguidedataevent_guidedataacquired"]
old-location: mstv\iguidedataevent_guidedataacquired.htm
tech.root: mstv
ms.assetid: 00f1aec7-4d26-4323-9d7e-c75d9a0c374c
ms.date: 12/05/2018
ms.keywords: GuideDataAcquired, GuideDataAcquired method [Microsoft TV Technologies], GuideDataAcquired method [Microsoft TV Technologies],IGuideDataEvent interface, IGuideDataEvent interface [Microsoft TV Technologies],GuideDataAcquired method, IGuideDataEvent.GuideDataAcquired, IGuideDataEvent::GuideDataAcquired, IGuideDataEventGuideDataAcquired, bdatif/IGuideDataEvent::GuideDataAcquired, mstv.iguidedataevent_guidedataacquired
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IGuideDataEvent::GuideDataAcquired
 - bdatif/IGuideDataEvent::GuideDataAcquired
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideDataEvent.GuideDataAcquired
---

# IGuideDataEvent::GuideDataAcquired


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GuideDataAcquired</b> method is called when a complete set of guide data has been acquired from the current transport stream.



Currently the <a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> (TIF) does not support this event, so this method is not called.



## -returns

Return S_OK if successful, or an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent Interface</a>
