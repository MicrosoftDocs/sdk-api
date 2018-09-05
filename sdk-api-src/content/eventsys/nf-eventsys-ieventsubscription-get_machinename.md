---
UID: NF:eventsys.IEventSubscription.get_MachineName
title: IEventSubscription::get_MachineName
author: windows-sdk-content
description: The name of the computer on which the subscriber should be activated (for a persistent subscription).
old-location: cos\ieventsubscription_machinename.htm
old-project: cossdk
ms.assetid: b56027ac-abe6-4d13-ad3a-254a2f92ab6d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEventSubscription interface [COM+],MachineName property, IEventSubscription.MachineName, IEventSubscription.get_MachineName, IEventSubscription::MachineName, IEventSubscription::get_MachineName, IEventSubscription::put_MachineName, MachineName property [COM+], MachineName property [COM+],IEventSubscription interface, cos.ieventsubscription_machinename, eventsys/IEventSubscription::MachineName, eventsys/IEventSubscription::get_MachineName, eventsys/IEventSubscription::put_MachineName, get_MachineName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: eventsys.h
req.include-header: 
req.redist: 
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
 - IEventSubscription.MachineName
 - IEventSubscription.get_MachineName
 - IEventSubscription.put_MachineName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventSubscription::get_MachineName


## -description


The name of the computer on which the subscriber should be activated (for a persistent subscription).

This property is read/write.


## -parameters


## -remarks



This information is only meaningful if the <a href="https://msdn.microsoft.com/004f662c-8fcb-4490-897b-48bf5ea306c7">SubscriberCLSID</a> property is not empty. This property has no effect on transient subscriptions.




## -see-also




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>
 

 

