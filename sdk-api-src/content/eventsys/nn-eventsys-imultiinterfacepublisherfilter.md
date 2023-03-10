---
UID: NN:eventsys.IMultiInterfacePublisherFilter
title: IMultiInterfacePublisherFilter (eventsys.h)
description: Manages a filtered subscription cache for an event method.
helpviewer_keywords: ["IMultiInterfacePublisherFilter","IMultiInterfacePublisherFilter interface [COM+]","IMultiInterfacePublisherFilter interface [COM+]","described","_cos_IMultiInterfacePublisherFilter","cos.imultiinterfacepublisherfilter","eventsys/IMultiInterfacePublisherFilter"]
old-location: cos\imultiinterfacepublisherfilter.htm
tech.root: cos
ms.assetid: f20f778b-fdd5-4c34-871b-d03cd1cd31cc
ms.date: 12/05/2018
ms.keywords: IMultiInterfacePublisherFilter, IMultiInterfacePublisherFilter interface [COM+], IMultiInterfacePublisherFilter interface [COM+],described, _cos_IMultiInterfacePublisherFilter, cos.imultiinterfacepublisherfilter, eventsys/IMultiInterfacePublisherFilter
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EventSys.idl
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
 - IMultiInterfacePublisherFilter
 - eventsys/IMultiInterfacePublisherFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EventSys.h
api_name:
 - IMultiInterfacePublisherFilter
---

# IMultiInterfacePublisherFilter interface


## -description

Manages a filtered subscription cache for an event method. Only subscribers who meet the criteria specified by the filter are notified when the associated event is fired. The <b>IMultiInterfacePublisherFilter</b> interface differs from the <a href="/windows/desktop/api/eventsys/nn-eventsys-ipublisherfilter">IPublisherFilter</a> interface in that it supports multiple event interfaces for the event object.

## -inheritance

The <b>IMultiInterfacePublisherFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMultiInterfacePublisherFilter</b> also has these types of members:

