---
UID: NN:eventsys.IPublisherFilter
title: IPublisherFilter (eventsys.h)
description: Acts as a callback interface so that event publishers can control which subscribers receive event notifications or the order in which subscribers are notified.
helpviewer_keywords: ["IPublisherFilter","IPublisherFilter interface [COM+]","IPublisherFilter interface [COM+]","described","_cos_IPublisherFilter","cos.ipublisherfilter","eventsys/IPublisherFilter"]
old-location: cos\ipublisherfilter.htm
tech.root: cos
ms.assetid: affc0af4-36f8-4479-8685-f91c29111d76
ms.date: 12/05/2018
ms.keywords: IPublisherFilter, IPublisherFilter interface [COM+], IPublisherFilter interface [COM+],described, _cos_IPublisherFilter, cos.ipublisherfilter, eventsys/IPublisherFilter
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
 - IPublisherFilter
 - eventsys/IPublisherFilter
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
 - IPublisherFilter
---

# IPublisherFilter interface


## -description

Acts as a callback interface so that event publishers can control which subscribers receive event notifications or the order in which subscribers are notified.


<b>IPublisherFilter</b> is supported only for backward compatibility. Instead, use the <a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a> interface.

## -inheritance

The <b>IPublisherFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPublisherFilter</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a>
