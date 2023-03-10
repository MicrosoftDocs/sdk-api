---
UID: NN:comsvcs.IMtsEvents
title: IMtsEvents (comsvcs.h)
description: Provides methods for obtaining information about the running package and establishing event sinks.
helpviewer_keywords: ["IMtsEvents","IMtsEvents interface [COM+]","IMtsEvents interface [COM+]","described","_dtc_IMtsEvents_Interface","comsvcs/IMtsEvents","cos.imtsevents"]
old-location: cos\imtsevents.htm
tech.root: cos
ms.assetid: 7db3a373-00d3-480e-8f8e-7e65a468d5dc
ms.date: 12/05/2018
ms.keywords: IMtsEvents, IMtsEvents interface [COM+], IMtsEvents interface [COM+],described, _dtc_IMtsEvents_Interface, comsvcs/IMtsEvents, cos.imtsevents
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
 - IMtsEvents
 - comsvcs/IMtsEvents
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
 - IMtsEvents
---

# IMtsEvents interface


## -description

Provides methods for obtaining information about the running package and establishing event sinks. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IMtsEvents</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMtsEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
