---
UID: NF:eventsys.IEventObjectCollection.Remove
title: IEventObjectCollection::Remove
author: windows-sdk-content
description: Removes an event object from the collection.
old-location: cos\ieventobjectcollection_remove.htm
tech.root: cossdk
ms.assetid: 5092b1e1-bbf2-493c-92be-41196b43d4f2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEventObjectCollection interface [COM+],Remove method, IEventObjectCollection.Remove, IEventObjectCollection::Remove, Remove, Remove method [COM+], Remove method [COM+],IEventObjectCollection interface, _cos_IEventObjectCollection_Remove, cos.ieventobjectcollection_remove, eventsys/IEventObjectCollection::Remove
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
req.idl: Eventsys.idl
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
 - Eventsys.h
api_name:
 - IEventObjectCollection.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEventObjectCollection::Remove


## -description


Removes an event object from the collection.


## -parameters




### -param objectID [in]

The ID property of the event object to be removed. For example, if the collection consists of subscription objects, this parameter would contain the SubscriptionID property of the event subscription object to be removed from the collection.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/7bb00b80-a48f-49c8-983d-9ff0ea424e4d">IEventObjectCollection</a>
 

 

