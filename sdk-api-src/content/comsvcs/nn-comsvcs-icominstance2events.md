---
UID: NN:comsvcs.IComInstance2Events
title: IComInstance2Events (comsvcs.h)
description: Notifies the subscriber if an object is created or released by a client.
helpviewer_keywords: ["IComInstance2Events","IComInstance2Events interface [COM+]","IComInstance2Events interface [COM+]","described","_dtc_icominstance2events","comsvcs/IComInstance2Events","cos.icominstance2events"]
old-location: cos\icominstance2events.htm
tech.root: cos
ms.assetid: 2fb2904d-7069-4303-bb3c-2caef9499c1e
ms.date: 12/05/2018
ms.keywords: IComInstance2Events, IComInstance2Events interface [COM+], IComInstance2Events interface [COM+],described, _dtc_icominstance2events, comsvcs/IComInstance2Events, cos.icominstance2events
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
 - IComInstance2Events
 - comsvcs/IComInstance2Events
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
 - IComInstance2Events
---

# IComInstance2Events interface


## -description

Notifies the subscriber if an object is created or released by a client. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComInstance2Events</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComInstance2Events</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
