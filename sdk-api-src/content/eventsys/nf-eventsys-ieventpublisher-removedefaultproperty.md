---
UID: NF:eventsys.IEventPublisher.RemoveDefaultProperty
title: IEventPublisher::RemoveDefaultProperty
author: windows-sdk-content
description: Removes a named property and its value from the property bag associated with the event publisher object.
old-location: com\ieventpublisher_removedefaultproperty.htm
old-project: com
ms.assetid: da691bac-e940-431d-acef-8c29f4a25c70
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IEventPublisher interface [COM],RemoveDefaultProperty method, IEventPublisher.RemoveDefaultProperty, IEventPublisher::RemoveDefaultProperty, RemoveDefaultProperty, RemoveDefaultProperty method [COM], RemoveDefaultProperty method [COM],IEventPublisher interface, _com_ieventpublisher_removedefaultproperty, com.ieventpublisher_removedefaultproperty, eventsys/IEventPublisher::RemoveDefaultProperty
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
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EventSys.h
api_name:
-	IEventPublisher.RemoveDefaultProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventPublisher::RemoveDefaultProperty


## -description


Removes a named property and its value from the property bag associated with the event publisher object.


## -parameters




### -param bstrPropertyName [in]

The name of the property to be removed.


## -returns



The possible return values include E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



An <a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">EventPublisher</a> object includes a property bag that can contain name and value pairs. Objects in the event system, including subscribers, can add, modify, and read these properties.




## -see-also




<a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">IEventPublisher</a>
 

 

