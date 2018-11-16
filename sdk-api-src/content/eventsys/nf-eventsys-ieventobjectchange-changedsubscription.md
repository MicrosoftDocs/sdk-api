---
UID: NF:eventsys.IEventObjectChange.ChangedSubscription
title: IEventObjectChange::ChangedSubscription
author: windows-sdk-content
description: Indicates that a subscription object has been added, modified, or deleted.
old-location: cos\ieventobjectchange_changedsubscription.htm
tech.root: cossdk
ms.assetid: 61d67705-b225-4f9e-98a5-cb636989f44f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ChangedSubscription, ChangedSubscription method [COM+], ChangedSubscription method [COM+],IEventObjectChange interface, IEventObjectChange interface [COM+],ChangedSubscription method, IEventObjectChange.ChangedSubscription, IEventObjectChange::ChangedSubscription, _cos_IEventObjectChange_ChangedSubscription, cos.ieventobjectchange_changedsubscription, eventsys/IEventObjectChange::ChangedSubscription
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
 - IEventObjectChange.ChangedSubscription
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
- IEventObjectChange.ChangedSubscription
: 
---

# IEventObjectChange::ChangedSubscription


## -description


Indicates that a subscription object has been added, modified, or deleted.



## -parameters




### -param changeType [in]

The type of change to the subscription object. Values are taken from the EOC_ChangeType enumeration. 


### -param bstrSubscriptionID [in]

The SubscriptionID property of the subscription object that changed.



## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2e916601-e03d-4c5f-a8fb-38317cfb66ad">IEventObjectChange</a>
 

 

