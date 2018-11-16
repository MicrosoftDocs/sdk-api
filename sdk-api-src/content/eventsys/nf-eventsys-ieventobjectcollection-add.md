---
UID: NF:eventsys.IEventObjectCollection.Add
title: IEventObjectCollection::Add
author: windows-sdk-content
description: Adds an event object to the collection.
old-location: cos\ieventobjectcollection_add.htm
tech.root: cossdk
ms.assetid: ca08e56a-2ade-4209-a61a-b9dae021e888
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Add, Add method [COM+], Add method [COM+],IEventObjectCollection interface, IEventObjectCollection interface [COM+],Add method, IEventObjectCollection.Add, IEventObjectCollection::Add, _cos_IEventObjectCollection_Add, cos.ieventobjectcollection_add, eventsys/IEventObjectCollection::Add
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
 - IEventObjectCollection.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- eventsys.h
: 
- IEventObjectCollection.Add
: 
---

# IEventObjectCollection::Add


## -description


Adds an event object to the collection.


## -parameters




### -param item [in]

A pointer to the event object to be added to the collection. This parameter cannot be <b>NULL</b>.


### -param objectID [in]

The ID property of the event object to be added. For example, if the collection consists of subscription objects, this parameter would contain the SubscriptionID property of the event subscription object to be added to the collection.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/7bb00b80-a48f-49c8-983d-9ff0ea424e4d">IEventObjectCollection</a>
 

 

