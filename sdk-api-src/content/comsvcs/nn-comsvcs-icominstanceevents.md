---
UID: NN:comsvcs.IComInstanceEvents
title: IComInstanceEvents (comsvcs.h)
description: Notifies the subscriber of an object's creation or release.
helpviewer_keywords: ["IComInstanceEvents","IComInstanceEvents interface [COM+]","IComInstanceEvents interface [COM+]","described","_dtc_IComInstanceEvents","comsvcs/IComInstanceEvents","cos.icominstanceevents"]
old-location: cos\icominstanceevents.htm
tech.root: cos
ms.assetid: 11e4559e-04c5-4fa9-b618-458ca7daf00e
ms.date: 12/05/2018
ms.keywords: IComInstanceEvents, IComInstanceEvents interface [COM+], IComInstanceEvents interface [COM+],described, _dtc_IComInstanceEvents, comsvcs/IComInstanceEvents, cos.icominstanceevents
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
 - IComInstanceEvents
 - comsvcs/IComInstanceEvents
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
 - IComInstanceEvents
---

# IComInstanceEvents interface


## -description

Notifies the subscriber of an object's creation or release. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComInstanceEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComInstanceEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
