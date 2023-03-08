---
UID: NN:comsvcs.IComExceptionEvents
title: IComExceptionEvents (comsvcs.h)
description: Notifies the subscriber when an unhandled exception occurs in the user's code.
helpviewer_keywords: ["IComExceptionEvents","IComExceptionEvents interface [COM+]","IComExceptionEvents interface [COM+]","described","_dtc_IComExceptionEvents","comsvcs/IComExceptionEvents","cos.icomexceptionevents"]
old-location: cos\icomexceptionevents.htm
tech.root: cos
ms.assetid: e484cad0-3b7e-4822-bbde-c953cb0301ca
ms.date: 12/05/2018
ms.keywords: IComExceptionEvents, IComExceptionEvents interface [COM+], IComExceptionEvents interface [COM+],described, _dtc_IComExceptionEvents, comsvcs/IComExceptionEvents, cos.icomexceptionevents
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
 - IComExceptionEvents
 - comsvcs/IComExceptionEvents
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
 - IComExceptionEvents
---

# IComExceptionEvents interface


## -description

Notifies the subscriber when an unhandled exception occurs in the user's code. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComExceptionEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComExceptionEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
