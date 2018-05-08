---
UID: NF:eventsys.IMultiInterfacePublisherFilter.Initialize
title: IMultiInterfacePublisherFilter::Initialize
author: windows-driver-content
description: Associates an event class with a publisher filter.
old-location: cos\imultiinterfacepublisherfilter_initialize.htm
old-project: cossdk
ms.assetid: d69075a3-7b5a-4c99-9e51-d07a3dde511a
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IMultiInterfacePublisherFilter interface [COM+],Initialize method, IMultiInterfacePublisherFilter.Initialize, IMultiInterfacePublisherFilter::Initialize, Initialize, Initialize method [COM+], Initialize method [COM+],IMultiInterfacePublisherFilter interface, _cos_IMultiInterfacePublisherFilter_Initialize, cos.imultiinterfacepublisherfilter_initialize, eventsys/IMultiInterfacePublisherFilter::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EventSys.h
api_name:
-	IMultiInterfacePublisherFilter.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMultiInterfacePublisherFilter::Initialize


## -description


Associates an event class with a publisher filter.


## -parameters




### -param pEIC






#### - pIEC [in]

A pointer to the <a href="https://msdn.microsoft.com/e603f68a-881c-468d-a3d3-738f43400e01">IMultiInterfaceEventControl</a> interface on an event class object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The publisher filter uses the pointer passed in <i>pIEC</i> to obtain a list of subscribers, by calling <a href="https://msdn.microsoft.com/38b1d0fe-c32e-41d5-a0c1-2b4e72908fce">IMultiInterfaceEventControl::GetSubscriptions</a>. 





## -see-also




<a href="https://msdn.microsoft.com/f20f778b-fdd5-4c34-871b-d03cd1cd31cc">IMultiInterfacePublisherFilter</a>
 

 

