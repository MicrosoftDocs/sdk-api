---
UID: NF:eventsys.IMultiInterfacePublisherFilter.PrepareToFire
title: IMultiInterfacePublisherFilter::PrepareToFire
author: windows-sdk-content
description: Prepares the publisher filter to begin firing a filtered list of subscriptions using a provided firing control. The firing control is contained in the event class object.
old-location: cos\imultiinterfacepublisherfilter_preparetofire.htm
old-project: cossdk
ms.assetid: a9257017-a9e7-4a0a-9dee-55493a659bda
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IMultiInterfacePublisherFilter interface [COM+],PrepareToFire method, IMultiInterfacePublisherFilter.PrepareToFire, IMultiInterfacePublisherFilter::PrepareToFire, PrepareToFire, PrepareToFire method [COM+], PrepareToFire method [COM+],IMultiInterfacePublisherFilter interface, _cos_MultiInterfacePublisherFilter_PrepareToFire, cos.imultiinterfacepublisherfilter_preparetofire, eventsys/IMultiInterfacePublisherFilter::PrepareToFire
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EOC_ChangeType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EventSys.h
api_name:
 - IMultiInterfacePublisherFilter.PrepareToFire
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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

A pointer to the <a href="https://msdn.microsoft.com/1db216b8-f334-4fa2-81db-0f6c1646b320">IFiringControl</a> interface on the firing control object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Prior to invoking the application event interface method, the event object invokes this method one time on the publisher filter for each published event.




## -see-also




<a href="https://msdn.microsoft.com/f20f778b-fdd5-4c34-871b-d03cd1cd31cc">IMultiInterfacePublisherFilter</a>
 

 

