---
UID: NF:eventsys.IEventPublisher.PutDefaultProperty
title: IEventPublisher::PutDefaultProperty
author: windows-sdk-content
description: Writes a named property and its value to the property bag associated with the event publisher.
old-location: com\ieventpublisher_putdefaultproperty.htm
tech.root: com
ms.assetid: 418f1c16-1b21-4023-b0fc-6e9082b8264e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IEventPublisher interface [COM],PutDefaultProperty method, IEventPublisher.PutDefaultProperty, IEventPublisher::PutDefaultProperty, PutDefaultProperty, PutDefaultProperty method [COM], PutDefaultProperty method [COM],IEventPublisher interface, _com_ieventpublisher_putdefaultproperty, com.ieventpublisher_putdefaultproperty, eventsys/IEventPublisher::PutDefaultProperty
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
 - IEventPublisher.PutDefaultProperty
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
- IEventPublisher.PutDefaultProperty
: 
---

# IEventPublisher::PutDefaultProperty


## -description


Writes a named property and its value to the property bag associated with the event publisher.


## -parameters




### -param bstrPropertyName [in]

The name of the property whose value is to be set.


### -param propertyValue [in]

The new value for the property.


## -returns



The possible return values include E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



An <a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">EventPublisher</a> object includes a property bag that can contain name and value pairs. Objects in the event system, including subscribers, can add, modify, and read these properties.




## -see-also




<a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">IEventPublisher</a>
 

 

