---
UID: NF:eventsys.IEventSubscription.put_MachineName
title: IEventSubscription::put_MachineName (eventsys.h)
author: windows-sdk-content
description: The name of the computer on which the subscriber should be activated (for a persistent subscription).
old-location: cos\ieventsubscription_machinename.htm
tech.root: cossdk
ms.assetid: b56027ac-abe6-4d13-ad3a-254a2f92ab6d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEventSubscription interface [COM+],MachineName property, IEventSubscription.MachineName, IEventSubscription.put_MachineName, IEventSubscription::MachineName, IEventSubscription::get_MachineName, IEventSubscription::put_MachineName, MachineName property [COM+], MachineName property [COM+],IEventSubscription interface, cos.ieventsubscription_machinename, eventsys/IEventSubscription::MachineName, eventsys/IEventSubscription::get_MachineName, eventsys/IEventSubscription::put_MachineName, put_MachineName
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
 - IEventSubscription.MachineName
 - IEventSubscription.get_MachineName
 - IEventSubscription.put_MachineName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventSubscription::put_MachineName


## -description


The name of the computer on which the subscriber should be activated (for a persistent subscription).

This property is read/write.


## -parameters


## -remarks



This information is only meaningful if the <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriberclsid">SubscriberCLSID</a> property is not empty. This property has no effect on transient subscriptions.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>
 

 

