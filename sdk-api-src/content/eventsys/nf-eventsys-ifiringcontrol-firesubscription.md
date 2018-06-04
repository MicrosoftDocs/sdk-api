---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFiringControl::FireSubscription


## -description


Fires an event to a single subscriber.


## -parameters




### -param subscription [in]

A pointer to the <a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a> interface on a subscription object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The <b>FireSubscription</b> method fires an event to the subscriber associated with the subscription object identified by the <i>subscription</i> parameter. A publisher filter typically iterates through a filtered list of subscriptions and calls <b>FireSubscription</b> for each associated subscriber. All standard delivery processing is done by the event object for the subscription, including the following: 



<ul>
<li>Any standard parameter filtering.
</li>
<li>Activating the subscriber object (optional, for persistent subscriptions).
</li>
<li>Depending on parameter filtering, invoking the event method that originally caused entry into the publisher filter on the subscriber.
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/1db216b8-f334-4fa2-81db-0f6c1646b320">IFiringControl</a>
 

 

