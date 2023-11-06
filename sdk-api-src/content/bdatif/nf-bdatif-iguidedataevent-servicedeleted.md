---
UID: NF:bdatif.IGuideDataEvent.ServiceDeleted
title: IGuideDataEvent::ServiceDeleted (bdatif.h)
description: The ServiceDeleted method is called when a service has been deleted.
helpviewer_keywords: ["IGuideDataEvent interface [Microsoft TV Technologies]","ServiceDeleted method","IGuideDataEvent.ServiceDeleted","IGuideDataEvent::ServiceDeleted","IGuideDataEventServiceDeleted","ServiceDeleted","ServiceDeleted method [Microsoft TV Technologies]","ServiceDeleted method [Microsoft TV Technologies]","IGuideDataEvent interface","bdatif/IGuideDataEvent::ServiceDeleted","mstv.iguidedataevent_servicedeleted"]
old-location: mstv\iguidedataevent_servicedeleted.htm
tech.root: mstv
ms.assetid: bba15ebe-d1c5-4c71-b052-6b75a7825613
ms.date: 12/05/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ServiceDeleted method, IGuideDataEvent.ServiceDeleted, IGuideDataEvent::ServiceDeleted, IGuideDataEventServiceDeleted, ServiceDeleted, ServiceDeleted method [Microsoft TV Technologies], ServiceDeleted method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ServiceDeleted, mstv.iguidedataevent_servicedeleted
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
 - IGuideDataEvent::ServiceDeleted
 - bdatif/IGuideDataEvent::ServiceDeleted
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
 - IGuideDataEvent.ServiceDeleted
---

# IGuideDataEvent::ServiceDeleted


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ServiceDeleted</b> method is called when a service has been deleted.



Currently the <a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> (TIF) does not support this event, so this method is not called.

## -parameters

### -param varServiceDescriptionID [in]

Specifies the unique identifier of the service that was deleted.

## -returns

Return S_OK if successful, or an error code.

## -remarks

The event sink is not required to support this event; it may return E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent Interface</a>