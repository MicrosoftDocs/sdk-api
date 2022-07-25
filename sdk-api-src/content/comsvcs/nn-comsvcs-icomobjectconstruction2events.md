---
UID: NN:comsvcs.IComObjectConstruction2Events
title: IComObjectConstruction2Events (comsvcs.h)
description: Notifies the subscriber if a constructed object is created.
helpviewer_keywords: ["IComObjectConstruction2Events","IComObjectConstruction2Events interface [COM+]","IComObjectConstruction2Events interface [COM+]","described","_dtc_icomobjectconstruction2events","comsvcs/IComObjectConstruction2Events","cos.icomobjectconstruction2events"]
old-location: cos\icomobjectconstruction2events.htm
tech.root: cos
ms.assetid: 976b8c1a-5ccd-48e2-a77c-10d4de9a4ffa
ms.date: 12/05/2018
ms.keywords: IComObjectConstruction2Events, IComObjectConstruction2Events interface [COM+], IComObjectConstruction2Events interface [COM+],described, _dtc_icomobjectconstruction2events, comsvcs/IComObjectConstruction2Events, cos.icomobjectconstruction2events
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
 - IComObjectConstruction2Events
 - comsvcs/IComObjectConstruction2Events
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
 - IComObjectConstruction2Events
---

# IComObjectConstruction2Events interface


## -description

Notifies the subscriber if a constructed object is created. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog. A constructed object is derived from the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectconstruct">IObjectConstruct</a> interface. Constructed objects can inherit parameter names from within other objects or libraries.

## -inheritance

The <b>IComObjectConstruction2Events</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComObjectConstruction2Events</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
