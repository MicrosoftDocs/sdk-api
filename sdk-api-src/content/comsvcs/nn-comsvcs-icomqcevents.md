---
UID: NN:comsvcs.IComQCEvents
title: IComQCEvents (comsvcs.h)
description: Notifies the subscriber if a queued message is created, de-queued, or moved to a retry or dead letter queue.
helpviewer_keywords: ["IComQCEvents","IComQCEvents interface [COM+]","IComQCEvents interface [COM+]","described","_dtc_IComQCEvents","comsvcs/IComQCEvents","cos.icomqcevents"]
old-location: cos\icomqcevents.htm
tech.root: cos
ms.assetid: d7c8220d-a302-4f95-b0b6-8d47f9f27da7
ms.date: 12/05/2018
ms.keywords: IComQCEvents, IComQCEvents interface [COM+], IComQCEvents interface [COM+],described, _dtc_IComQCEvents, comsvcs/IComQCEvents, cos.icomqcevents
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
 - IComQCEvents
 - comsvcs/IComQCEvents
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
 - IComQCEvents
---

# IComQCEvents interface


## -description

Notifies the subscriber if a queued message is created, de-queued, or moved to a retry or dead letter queue. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComQCEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComQCEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>



<a href="/windows/desktop/cossdk/com--queued-components">COM+ Queued Components</a>
