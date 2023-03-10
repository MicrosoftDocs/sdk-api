---
UID: NN:comsvcs.IComThreadEvents
title: IComThreadEvents (comsvcs.h)
description: Notifies the subscriber if a single-threaded apartment (STA) is created or terminated, and when an apartment thread is allocated.
helpviewer_keywords: ["IComThreadEvents","IComThreadEvents interface [COM+]","IComThreadEvents interface [COM+]","described","_dtc_IComThreadEvents","comsvcs/IComThreadEvents","cos.icomthreadevents"]
old-location: cos\icomthreadevents.htm
tech.root: cos
ms.assetid: a6523088-cca4-41c1-a3fe-d8cb7320ff33
ms.date: 12/05/2018
ms.keywords: IComThreadEvents, IComThreadEvents interface [COM+], IComThreadEvents interface [COM+],described, _dtc_IComThreadEvents, comsvcs/IComThreadEvents, cos.icomthreadevents
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
 - IComThreadEvents
 - comsvcs/IComThreadEvents
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
 - IComThreadEvents
---

# IComThreadEvents interface


## -description

Notifies the subscriber if a single-threaded apartment (STA) is created or terminated, and when an apartment thread is allocated. The subscriber is also notified if an activity is assigned or unassigned to an apartment thread. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComThreadEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComThreadEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
