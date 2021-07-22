---
UID: NN:comsvcs.IComApp2Events
title: IComApp2Events (comsvcs.h)
description: Notifies the subscriber if a COM+ server application is loaded, shut down, or paused.
helpviewer_keywords: ["IComApp2Events","IComApp2Events interface [COM+]","IComApp2Events interface [COM+]","described","_dtc_icomapp2events","comsvcs/IComApp2Events","cos.icomapp2events"]
old-location: cos\icomapp2events.htm
tech.root: cos
ms.assetid: 45e0d26b-7485-436b-9b64-fa48217b32d1
ms.date: 12/05/2018
ms.keywords: IComApp2Events, IComApp2Events interface [COM+], IComApp2Events interface [COM+],described, _dtc_icomapp2events, comsvcs/IComApp2Events, cos.icomapp2events
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
 - IComApp2Events
 - comsvcs/IComApp2Events
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
 - IComApp2Events
---

# IComApp2Events interface


## -description

Notifies the subscriber if a COM+ server application is loaded, shut down, or paused. The subscriber is also notified if the application is marked for recycling. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComApp2Events</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComApp2Events</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
