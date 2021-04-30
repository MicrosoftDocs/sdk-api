---
UID: NF:eventsys.IMultiInterfacePublisherFilter.PrepareToFire
title: IMultiInterfacePublisherFilter::PrepareToFire (eventsys.h)
description: Prepares the publisher filter to begin firing a filtered list of subscriptions using a provided firing control. The firing control is contained in the event class object.
helpviewer_keywords: ["IMultiInterfacePublisherFilter interface [COM+]","PrepareToFire method","IMultiInterfacePublisherFilter.PrepareToFire","IMultiInterfacePublisherFilter::PrepareToFire","PrepareToFire","PrepareToFire method [COM+]","PrepareToFire method [COM+]","IMultiInterfacePublisherFilter interface","_cos_MultiInterfacePublisherFilter_PrepareToFire","cos.imultiinterfacepublisherfilter_preparetofire","eventsys/IMultiInterfacePublisherFilter::PrepareToFire"]
old-location: cos\imultiinterfacepublisherfilter_preparetofire.htm
tech.root: cos
ms.assetid: a9257017-a9e7-4a0a-9dee-55493a659bda
ms.date: 12/05/2018
ms.keywords: IMultiInterfacePublisherFilter interface [COM+],PrepareToFire method, IMultiInterfacePublisherFilter.PrepareToFire, IMultiInterfacePublisherFilter::PrepareToFire, PrepareToFire, PrepareToFire method [COM+], PrepareToFire method [COM+],IMultiInterfacePublisherFilter interface, _cos_MultiInterfacePublisherFilter_PrepareToFire, cos.imultiinterfacepublisherfilter_preparetofire, eventsys/IMultiInterfacePublisherFilter::PrepareToFire
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
 - IMultiInterfacePublisherFilter::PrepareToFire
 - eventsys/IMultiInterfacePublisherFilter::PrepareToFire
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
 - IMultiInterfacePublisherFilter.PrepareToFire
---

# IMultiInterfacePublisherFilter::PrepareToFire


## -description

Prepares the publisher filter to begin firing a filtered list of subscriptions using a provided firing control. The firing control is contained in the event class object.

## -parameters

### -param iid [in]

The interface ID of the interface being fired.

### -param methodName [in]

The name of the event method to be fired.

### -param firingControl [in]

A pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ifiringcontrol">IFiringControl</a> interface on the firing control object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Prior to invoking the application event interface method, the event object invokes this method one time on the publisher filter for each published event.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a>