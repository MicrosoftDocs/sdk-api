---
UID: NF:eventsys.IEventObjectChange.ChangedEventClass
title: IEventObjectChange::ChangedEventClass
author: windows-sdk-content
description: Indicates that an event class object has been added, modified, or deleted.
old-location: cos\ieventobjectchange_changedeventclass.htm
old-project: cossdk
ms.assetid: 8db711c8-7c01-4fb0-975c-a66c83063124
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ChangedEventClass, ChangedEventClass method [COM+], ChangedEventClass method [COM+],IEventObjectChange interface, IEventObjectChange interface [COM+],ChangedEventClass method, IEventObjectChange.ChangedEventClass, IEventObjectChange::ChangedEventClass, _cos_IEventObjectChange_ChangedEventClass, cos.ieventobjectchange_changedeventclass, eventsys/IEventObjectChange::ChangedEventClass
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
req.idl: Eventsys.idl
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
 - Eventsys.h
api_name:
 - IEventObjectChange.ChangedEventClass
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventObjectChange::ChangedEventClass


## -description


Indicates that an event class object has been added, modified, or deleted.


## -parameters




### -param changeType [in]

The type of change to the event class object. Values are taken from the <a href="https://msdn.microsoft.com/99a32590-6875-40ab-997a-c940b25b5de9">EOC_ChangeType</a> enumeration.


### -param bstrEventClassID [in]

The EventClassID property of the event class object that changed.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2e916601-e03d-4c5f-a8fb-38317cfb66ad">IEventObjectChange</a>
 

 

