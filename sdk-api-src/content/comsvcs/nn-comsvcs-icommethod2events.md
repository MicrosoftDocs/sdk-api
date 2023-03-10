---
UID: NN:comsvcs.IComMethod2Events
title: IComMethod2Events (comsvcs.h)
description: Notifies the subscriber if an object's method has been called, returned, or generated an exception. (IComMethod2Events)
helpviewer_keywords: ["IComMethod2Events","IComMethod2Events interface [COM+]","IComMethod2Events interface [COM+]","described","_dtc_IComMethod2Events","comsvcs/IComMethod2Events","cos.icommethod2events"]
old-location: cos\icommethod2events.htm
tech.root: cos
ms.assetid: e0642cb2-d5f2-4e4b-ad35-7818983ed467
ms.date: 12/05/2018
ms.keywords: IComMethod2Events, IComMethod2Events interface [COM+], IComMethod2Events interface [COM+],described, _dtc_IComMethod2Events, comsvcs/IComMethod2Events, cos.icommethod2events
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
 - IComMethod2Events
 - comsvcs/IComMethod2Events
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
 - IComMethod2Events
---

# IComMethod2Events interface


## -description

Notifies the subscriber if an object's method has been called, returned, or generated an exception. This interface extends the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icommethodevents">IComMethodEvents</a> interface to provide thread information. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComMethod2Events</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComMethod2Events</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
