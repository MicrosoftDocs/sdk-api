---
UID: NN:comsvcs.IComMethodEvents
title: IComMethodEvents (comsvcs.h)
description: Notifies the subscriber if an object's method has been called, returned, or generated an exception. (IComMethodEvents)
helpviewer_keywords: ["IComMethodEvents","IComMethodEvents interface [COM+]","IComMethodEvents interface [COM+]","described","_dtc_IComMethodEvents","comsvcs/IComMethodEvents","cos.icommethodevents"]
old-location: cos\icommethodevents.htm
tech.root: cos
ms.assetid: 24670a23-4300-48f9-a089-dff3082cb544
ms.date: 12/05/2018
ms.keywords: IComMethodEvents, IComMethodEvents interface [COM+], IComMethodEvents interface [COM+],described, _dtc_IComMethodEvents, comsvcs/IComMethodEvents, cos.icommethodevents
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
 - IComMethodEvents
 - comsvcs/IComMethodEvents
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
 - IComMethodEvents
---

# IComMethodEvents interface


## -description

Notifies the subscriber if an object's method has been called, returned, or generated an exception. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComMethodEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComMethodEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
