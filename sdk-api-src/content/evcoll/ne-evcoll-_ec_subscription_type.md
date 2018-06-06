---
UID: NE:evcoll._EC_SUBSCRIPTION_TYPE
title: "_EC_SUBSCRIPTION_TYPE"
author: windows-sdk-content
description: Specifies the type of subscription to use (a source initiated or collector initiated subscription).
old-location: wec\ec_subscription_type.htm
old-project: WEC
ms.assetid: b9906fd8-10d4-4bdd-97b9-fb1ae9d4c588
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EC_SUBSCRIPTION_TYPE, EC_SUBSCRIPTION_TYPE enumeration, EcSubscriptionTypeCollectorInitiated, EcSubscriptionTypeSourceInitiated, _EC_SUBSCRIPTION_TYPE, evcoll/EC_SUBSCRIPTION_TYPE, evcoll/EcSubscriptionTypeCollectorInitiated, evcoll/EcSubscriptionTypeSourceInitiated, wec.ec_subscription_type, wes.ec_subscription_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: evcoll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EC_SUBSCRIPTION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_SUBSCRIPTION_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EC_SUBSCRIPTION_TYPE enumeration


## -description


The <b>EC_SUBSCRIPTION_TYPE</b> enumeration specifies the type of subscription to use (a source initiated or collector initiated subscription).


## -enum-fields




### -field EcSubscriptionTypeSourceInitiated

Allows you to define an event subscription on an event collector computer without defining the event source computers. Multiple remote event source computers can then be set up (using a group policy setting) to forward events to the event collector computer. For more information, see <a href="https://msdn.microsoft.com/c02b5075-d685-44cf-937f-a1edfd2550ca">Setting up a Source Initiated Subscription</a>. This subscription type is useful when you do not know or you do not want to specify  all the event sources computers that will forward events.


### -field EcSubscriptionTypeCollectorInitiated

The computer that receives forwarded events from event sources (other computers that the events were published on) initiates the subscription. You specify all the event sources at the time the subscription is created.

