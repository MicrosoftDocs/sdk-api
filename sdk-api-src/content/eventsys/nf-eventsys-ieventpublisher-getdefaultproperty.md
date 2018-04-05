---
UID: NF:eventsys.IEventPublisher.GetDefaultProperty
title: IEventPublisher::GetDefaultProperty method
author: windows-driver-content
description: Retrieves a named property and its value from the property bag associated with the event publisher.
old-location: com\ieventpublisher_getdefaultproperty.htm
old-project: com
ms.assetid: 5d9adc4f-30c9-42bd-89c9-e35384885b8c
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetDefaultProperty method [COM], GetDefaultProperty method [COM], IEventPublisher interface, GetDefaultProperty,IEventPublisher.GetDefaultProperty, IEventPublisher, IEventPublisher interface [COM], GetDefaultProperty method, IEventPublisher::GetDefaultProperty, _com_ieventpublisher_getdefaultproperty, com.ieventpublisher_getdefaultproperty, eventsys/IEventPublisher::GetDefaultProperty
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
-	IEventPublisher.GetDefaultProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventPublisher::GetDefaultProperty method


## -description


Retrieves a named property and its value from the property bag associated with the event publisher.


## -parameters




### -param bstrPropertyName [in]

The name of the property whose value is to be retrieved.


### -param propertyValue [out, retval]

A pointer to the variable that receives the property.


## -returns



The possible return values include E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



An <a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">EventPublisher</a> object includes a property bag that can contain name and value pairs. Objects in the event system, including subscribers, can add, modify, and read these properties.




## -see-also




<a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">IEventPublisher</a>
 

 

