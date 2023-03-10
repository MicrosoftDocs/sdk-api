---
UID: NN:comsvcs.IComObjectPool2Events
title: IComObjectPool2Events (comsvcs.h)
description: Notifies the subscriber if a transactional or non-transactional object is added to or obtained from the object pool.
helpviewer_keywords: ["IComObjectPool2Events","IComObjectPool2Events interface [COM+]","IComObjectPool2Events interface [COM+]","described","_dtc_icomobjectpool2events","comsvcs/IComObjectPool2Events","cos.icomobjectpool2events"]
old-location: cos\icomobjectpool2events.htm
tech.root: cos
ms.assetid: 2aac494d-52ce-408c-8444-8792b5b53604
ms.date: 12/05/2018
ms.keywords: IComObjectPool2Events, IComObjectPool2Events interface [COM+], IComObjectPool2Events interface [COM+],described, _dtc_icomobjectpool2events, comsvcs/IComObjectPool2Events, cos.icomobjectpool2events
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
 - IComObjectPool2Events
 - comsvcs/IComObjectPool2Events
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
 - IComObjectPool2Events
---

# IComObjectPool2Events interface


## -description

Notifies the subscriber if a transactional or non-transactional object is added to or obtained from the object pool. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComObjectPool2Events</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComObjectPool2Events</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
