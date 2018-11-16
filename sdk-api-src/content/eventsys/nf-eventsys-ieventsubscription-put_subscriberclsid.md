---
UID: NF:eventsys.IEventSubscription.put_SubscriberCLSID
title: IEventSubscription::put_SubscriberCLSID
author: windows-sdk-content
description: The CLSID of the subscriber component (for a persistent subscription).
old-location: cos\ieventsubscription_subscriberclsid.htm
tech.root: cossdk
ms.assetid: 004f662c-8fcb-4490-897b-48bf5ea306c7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEventSubscription interface [COM+],SubscriberCLSID property, IEventSubscription.SubscriberCLSID, IEventSubscription.put_SubscriberCLSID, IEventSubscription::SubscriberCLSID, IEventSubscription::get_SubscriberCLSID, IEventSubscription::put_SubscriberCLSID, SubscriberCLSID property [COM+], SubscriberCLSID property [COM+],IEventSubscription interface, cos.ieventsubscription_subscriberclsid, eventsys/IEventSubscription::SubscriberCLSID, eventsys/IEventSubscription::get_SubscriberCLSID, eventsys/IEventSubscription::put_SubscriberCLSID, put_SubscriberCLSID
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
 - IEventSubscription.SubscriberCLSID
 - IEventSubscription.get_SubscriberCLSID
 - IEventSubscription.put_SubscriberCLSID
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
- IEventSubscription.put_SubscriberCLSID
: 
---

# IEventSubscription::put_SubscriberCLSID


## -description


The CLSID of the subscriber component (for a persistent subscription).

This property is read/write.


## -parameters


## -remarks



If not empty, the subscription is persistent and the <a href="https://msdn.microsoft.com/207c8e74-d8f8-4576-8f2d-762c97bc048f">SubscriberInterface</a> property must be <b>NULL</b>. This property works in conjunction with the <a href="https://msdn.microsoft.com/b56027ac-abe6-4d13-ad3a-254a2f92ab6d">MachineName</a> property in a persistent subscription.




## -see-also




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>
 

 

