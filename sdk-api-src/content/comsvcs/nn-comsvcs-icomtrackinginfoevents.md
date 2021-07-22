---
UID: NN:comsvcs.IComTrackingInfoEvents
title: IComTrackingInfoEvents (comsvcs.h)
description: Notifies the subscriber when the tracking information for a collection changes.
helpviewer_keywords: ["IComTrackingInfoEvents","IComTrackingInfoEvents interface [COM+]","IComTrackingInfoEvents interface [COM+]","described","_dtc_IComTrackingInfoEvents","comsvcs/IComTrackingInfoEvents","cos.icomtrackinginfoevents"]
old-location: cos\icomtrackinginfoevents.htm
tech.root: cos
ms.assetid: bed709ca-5083-4073-a9f9-2b7b7f14cf87
ms.date: 12/05/2018
ms.keywords: IComTrackingInfoEvents, IComTrackingInfoEvents interface [COM+], IComTrackingInfoEvents interface [COM+],described, _dtc_IComTrackingInfoEvents, comsvcs/IComTrackingInfoEvents, cos.icomtrackinginfoevents
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IComTrackingInfoEvents
 - comsvcs/IComTrackingInfoEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComTrackingInfoEvents
---

# IComTrackingInfoEvents interface


## -description

Notifies the subscriber when the tracking information for a collection changes. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComTrackingInfoEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComTrackingInfoEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
