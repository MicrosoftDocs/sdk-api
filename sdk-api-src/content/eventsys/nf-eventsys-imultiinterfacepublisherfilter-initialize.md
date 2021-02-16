---
UID: NF:eventsys.IMultiInterfacePublisherFilter.Initialize
title: IMultiInterfacePublisherFilter::Initialize (eventsys.h)
description: Associates an event class with a publisher filter.
helpviewer_keywords: ["IMultiInterfacePublisherFilter interface [COM+]","Initialize method","IMultiInterfacePublisherFilter.Initialize","IMultiInterfacePublisherFilter::Initialize","Initialize","Initialize method [COM+]","Initialize method [COM+]","IMultiInterfacePublisherFilter interface","_cos_IMultiInterfacePublisherFilter_Initialize","cos.imultiinterfacepublisherfilter_initialize","eventsys/IMultiInterfacePublisherFilter::Initialize"]
old-location: cos\imultiinterfacepublisherfilter_initialize.htm
tech.root: cos
ms.assetid: d69075a3-7b5a-4c99-9e51-d07a3dde511a
ms.date: 12/05/2018
ms.keywords: IMultiInterfacePublisherFilter interface [COM+],Initialize method, IMultiInterfacePublisherFilter.Initialize, IMultiInterfacePublisherFilter::Initialize, Initialize, Initialize method [COM+], Initialize method [COM+],IMultiInterfacePublisherFilter interface, _cos_IMultiInterfacePublisherFilter_Initialize, cos.imultiinterfacepublisherfilter_initialize, eventsys/IMultiInterfacePublisherFilter::Initialize
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
 - IMultiInterfacePublisherFilter::Initialize
 - eventsys/IMultiInterfacePublisherFilter::Initialize
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
 - IMultiInterfacePublisherFilter.Initialize
---

# IMultiInterfacePublisherFilter::Initialize


## -description

Associates an event class with a publisher filter.

## -parameters

### -param pEIC [in]

A pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfaceeventcontrol">IMultiInterfaceEventControl</a> interface on an event class object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The publisher filter uses the pointer passed in <i>pIEC</i> to obtain a list of subscribers, by calling <a href="/windows/desktop/api/eventsys/nf-eventsys-imultiinterfaceeventcontrol-getsubscriptions">IMultiInterfaceEventControl::GetSubscriptions</a>.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a>