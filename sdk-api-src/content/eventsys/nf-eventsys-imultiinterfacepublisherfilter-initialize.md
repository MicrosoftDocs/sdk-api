---
UID: NF:eventsys.IMultiInterfacePublisherFilter.Initialize
title: IMultiInterfacePublisherFilter::Initialize (eventsys.h)
author: windows-sdk-content
description: Associates an event class with a publisher filter.
old-location: cos\imultiinterfacepublisherfilter_initialize.htm
tech.root: cossdk
ms.assetid: d69075a3-7b5a-4c99-9e51-d07a3dde511a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMultiInterfacePublisherFilter interface [COM+],Initialize method, IMultiInterfacePublisherFilter.Initialize, IMultiInterfacePublisherFilter::Initialize, Initialize, Initialize method [COM+], Initialize method [COM+],IMultiInterfacePublisherFilter interface, _cos_IMultiInterfacePublisherFilter_Initialize, cos.imultiinterfacepublisherfilter_initialize, eventsys/IMultiInterfacePublisherFilter::Initialize
ms.topic: method
f1_keywords: 
 - "eventsys/IMultiInterfacePublisherFilter.Initialize"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EventSys.h
api_name:
 - IMultiInterfacePublisherFilter.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMultiInterfacePublisherFilter::Initialize


## -description


Associates an event class with a publisher filter.


## -parameters




### -param pEIC [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-imultiinterfaceeventcontrol">IMultiInterfaceEventControl</a> interface on an event class object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The publisher filter uses the pointer passed in <i>pIEC</i> to obtain a list of subscribers, by calling <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-imultiinterfaceeventcontrol-getsubscriptions">IMultiInterfaceEventControl::GetSubscriptions</a>. 





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a>
 

 

