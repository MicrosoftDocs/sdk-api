---
UID: NF:eventsys.IFiringControl.FireSubscription
title: IFiringControl::FireSubscription
author: windows-sdk-content
description: Fires an event to a single subscriber.
old-location: cos\ifiringcontrol_firesubscription.htm
old-project: cossdk
ms.assetid: 64aaa99c-70e0-4a96-ab16-2f5b5666d1c4
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FireSubscription, FireSubscription method [COM+], FireSubscription method [COM+],IFiringControl interface, IFiringControl interface [COM+],FireSubscription method, IFiringControl.FireSubscription, IFiringControl::FireSubscription, _cos_IFiringControl_FireSubscriptio, cos.ifiringcontrol_firesubscription, eventsys/IFiringControl::FireSubscription
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
 - IFiringControl.FireSubscription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

