---
UID: NN:eventsys.IEventClass
title: IEventClass (eventsys.h)
description: Associates a class of event objects with the event interface those objects implement.
helpviewer_keywords: ["IEventClass","IEventClass interface [COM+]","IEventClass interface [COM+]","described","_cos_IEventClass","cos.ieventclass","eventsys/IEventClass"]
old-location: cos\ieventclass.htm
tech.root: cos
ms.assetid: e8c1fcd1-59fb-49d6-94b9-52b7c8551651
ms.date: 12/05/2018
ms.keywords: IEventClass, IEventClass interface [COM+], IEventClass interface [COM+],described, _cos_IEventClass, cos.ieventclass, eventsys/IEventClass
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Eventsys.idl
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
 - IEventClass
 - eventsys/IEventClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - eventsys.h
api_name:
 - IEventClass
---

# IEventClass interface


## -description

Associates a class of event objects with the event interface those objects implement.

<b>IEventClass</b> is the interface that is implemented by the CLSID_CEventClass objects, which are different than event class objects that are co-created by a publisher for the purpose of firing events.

An event object implements the <a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfaceeventcontrol">IMultiInterfaceEventControl</a> event interface. While this object can be used to configure event classes in the event store, the preferred method is to use the COM+ Administration interfaces. However, not all of the properties exposed by the <b>IEventClass</b> interface are available through the COM+ Administration interfaces.

## -see-also

<a href="/windows/desktop/cossdk/com--administration-interfaces">COM+ Administration Interfaces</a>