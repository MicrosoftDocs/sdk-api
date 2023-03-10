---
UID: NN:comsvcs.IComObjectConstructionEvents
title: IComObjectConstructionEvents (comsvcs.h)
description: Notifies the subscriber if a constructed object is created in an object pool.
helpviewer_keywords: ["IComObjectConstructionEvents","IComObjectConstructionEvents interface [COM+]","IComObjectConstructionEvents interface [COM+]","described","_dtc_IComObjectConstructionEvents","comsvcs/IComObjectConstructionEvents","cos.icomobjectconstructionevents"]
old-location: cos\icomobjectconstructionevents.htm
tech.root: cos
ms.assetid: c5fdb9b1-937e-43cb-93ff-e90f8c268fee
ms.date: 12/05/2018
ms.keywords: IComObjectConstructionEvents, IComObjectConstructionEvents interface [COM+], IComObjectConstructionEvents interface [COM+],described, _dtc_IComObjectConstructionEvents, comsvcs/IComObjectConstructionEvents, cos.icomobjectconstructionevents
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
 - IComObjectConstructionEvents
 - comsvcs/IComObjectConstructionEvents
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
 - IComObjectConstructionEvents
---

# IComObjectConstructionEvents interface


## -description

Notifies the subscriber if a constructed object is created in an object pool. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog. A constructed object is derived from the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectconstruct">IObjectConstruct</a> interface. Constructed objects can inherit parameter names from within other objects or libraries.

## -inheritance

The <b>IComObjectConstructionEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComObjectConstructionEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
