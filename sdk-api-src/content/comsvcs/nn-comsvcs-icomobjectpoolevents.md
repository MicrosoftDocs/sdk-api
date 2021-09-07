---
UID: NN:comsvcs.IComObjectPoolEvents
title: IComObjectPoolEvents (comsvcs.h)
description: Notifies the subscriber when a new object is added to the pool.
helpviewer_keywords: ["IComObjectPoolEvents","IComObjectPoolEvents interface [COM+]","IComObjectPoolEvents interface [COM+]","described","_dtc_IComObjectPoolEvents","comsvcs/IComObjectPoolEvents","cos.icomobjectpoolevents"]
old-location: cos\icomobjectpoolevents.htm
tech.root: cos
ms.assetid: a830b40b-a1b1-464e-b532-91cebd4e5d2f
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents, IComObjectPoolEvents interface [COM+], IComObjectPoolEvents interface [COM+],described, _dtc_IComObjectPoolEvents, comsvcs/IComObjectPoolEvents, cos.icomobjectpoolevents
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
 - IComObjectPoolEvents
 - comsvcs/IComObjectPoolEvents
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
 - IComObjectPoolEvents
---

# IComObjectPoolEvents interface


## -description

Notifies the subscriber when a new object is added to the pool. The subscriber is also notified when a transactional or non-transactional object is obtained or returned to the pool. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComObjectPoolEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComObjectPoolEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
