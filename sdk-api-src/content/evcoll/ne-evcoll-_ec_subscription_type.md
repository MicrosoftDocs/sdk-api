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

# _EC_SUBSCRIPTION_TYPE enumeration


## -description


The <b>EC_SUBSCRIPTION_TYPE</b> enumeration specifies the type of subscription to use (a source initiated or collector initiated subscription).


## -enum-fields




### -field EcSubscriptionTypeSourceInitiated

Allows you to define an event subscription on an event collector computer without defining the event source computers. Multiple remote event source computers can then be set up (using a group policy setting) to forward events to the event collector computer. For more information, see <a href="https://msdn.microsoft.com/c02b5075-d685-44cf-937f-a1edfd2550ca">Setting up a Source Initiated Subscription</a>. This subscription type is useful when you do not know or you do not want to specify  all the event sources computers that will forward events.


### -field EcSubscriptionTypeCollectorInitiated

The computer that receives forwarded events from event sources (other computers that the events were published on) initiates the subscription. You specify all the event sources at the time the subscription is created.

