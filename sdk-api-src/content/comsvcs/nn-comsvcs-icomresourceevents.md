---
UID: NN:comsvcs.IComResourceEvents
title: IComResourceEvents (comsvcs.h)
description: Notifies the subscriber if a resource is created, allocated, tracked, or destroyed.
helpviewer_keywords: ["IComResourceEvents","IComResourceEvents interface [COM+]","IComResourceEvents interface [COM+]","described","_dtc_IComResourceEvents","comsvcs/IComResourceEvents","cos.icomresourceevents"]
old-location: cos\icomresourceevents.htm
tech.root: cos
ms.assetid: fdc664b6-0459-4cbd-8e9e-0c3fe82e4321
ms.date: 12/05/2018
ms.keywords: IComResourceEvents, IComResourceEvents interface [COM+], IComResourceEvents interface [COM+],described, _dtc_IComResourceEvents, comsvcs/IComResourceEvents, cos.icomresourceevents
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IComResourceEvents
 - comsvcs/IComResourceEvents
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
 - IComResourceEvents
---

# IComResourceEvents interface


## -description

Notifies the subscriber if a resource is created, allocated, tracked, or destroyed. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComResourceEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComResourceEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
