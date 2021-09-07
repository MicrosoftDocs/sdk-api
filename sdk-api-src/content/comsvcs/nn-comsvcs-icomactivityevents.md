---
UID: NN:comsvcs.IComActivityEvents
title: IComActivityEvents (comsvcs.h)
description: Notifies the subscriber if an activity is created, destroyed, or timed out.
helpviewer_keywords: ["IComActivityEvents","IComActivityEvents interface [COM+]","IComActivityEvents interface [COM+]","described","_dtc_IComActivityEvents","comsvcs/IComActivityEvents","cos.icomactivityevents"]
old-location: cos\icomactivityevents.htm
tech.root: cos
ms.assetid: 9b702bcd-d5a6-41fa-98ce-00a245dfe770
ms.date: 12/05/2018
ms.keywords: IComActivityEvents, IComActivityEvents interface [COM+], IComActivityEvents interface [COM+],described, _dtc_IComActivityEvents, comsvcs/IComActivityEvents, cos.icomactivityevents
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
 - IComActivityEvents
 - comsvcs/IComActivityEvents
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
 - IComActivityEvents
---

# IComActivityEvents interface


## -description

Notifies the subscriber if an activity is created, destroyed, or timed out. The activity event is published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComActivityEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComActivityEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
