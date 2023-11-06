---
UID: NF:bdatif.IGuideDataEvent.ServiceChanged
title: IGuideDataEvent::ServiceChanged (bdatif.h)
description: The ServiceChanged method is called when a service has been changed.
helpviewer_keywords: ["IGuideDataEvent interface [Microsoft TV Technologies]","ServiceChanged method","IGuideDataEvent.ServiceChanged","IGuideDataEvent::ServiceChanged","IGuideDataEventServiceChanged","ServiceChanged","ServiceChanged method [Microsoft TV Technologies]","ServiceChanged method [Microsoft TV Technologies]","IGuideDataEvent interface","bdatif/IGuideDataEvent::ServiceChanged","mstv.iguidedataevent_servicechanged"]
old-location: mstv\iguidedataevent_servicechanged.htm
tech.root: mstv
ms.assetid: 75387dd8-e0e2-4fae-8c4a-a0b7b06f61b1
ms.date: 12/05/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ServiceChanged method, IGuideDataEvent.ServiceChanged, IGuideDataEvent::ServiceChanged, IGuideDataEventServiceChanged, ServiceChanged, ServiceChanged method [Microsoft TV Technologies], ServiceChanged method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ServiceChanged, mstv.iguidedataevent_servicechanged
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
 - IGuideDataEvent::ServiceChanged
 - bdatif/IGuideDataEvent::ServiceChanged
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
 - IGuideDataEvent.ServiceChanged
---

# IGuideDataEvent::ServiceChanged


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ServiceChanged</b> method is called when a service has been changed.

## -parameters

### -param varServiceDescriptionID [in]

Specifies the unique identifier of the service that has changed.

## -returns

Return S_OK if successful, or an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent Interface</a>