---
UID: NF:eventsys.IEventObjectChange.ChangedPublisher
title: IEventObjectChange::ChangedPublisher
author: windows-sdk-content
description: Indicates a publisher object has been added, modified, or deleted.
old-location: cos\ieventobjectchange_changedpublisher.htm
tech.root: cossdk
ms.assetid: 13bd95e6-5fc2-41e2-9002-67a87f727528
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ChangedPublisher, ChangedPublisher method [COM+], ChangedPublisher method [COM+],IEventObjectChange interface, IEventObjectChange interface [COM+],ChangedPublisher method, IEventObjectChange.ChangedPublisher, IEventObjectChange::ChangedPublisher, _cos_ieventobjectchange_changedpublisher, cos.ieventobjectchange_changedpublisher, eventsys/IEventObjectChange::ChangedPublisher
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
 - IEventObjectChange.ChangedPublisher
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEventObjectChange::ChangedPublisher


## -description


Indicates a publisher object has been added, modified, or deleted.


## -parameters




### -param changeType [in]

The type of change to the publisher object. Values are taken from the <a href="https://msdn.microsoft.com/99a32590-6875-40ab-997a-c940b25b5de9">EOC_ChangeType</a> enumeration.


### -param bstrPublisherID [in]

The PublisherID property of the publisher object that changed.



## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2e916601-e03d-4c5f-a8fb-38317cfb66ad">IEventObjectChange</a>
 

 

