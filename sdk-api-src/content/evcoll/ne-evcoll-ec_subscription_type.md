---
UID: NE:evcoll._EC_SUBSCRIPTION_TYPE
title: EC_SUBSCRIPTION_TYPE (evcoll.h)
description: Specifies the type of subscription to use (a source initiated or collector initiated subscription).
helpviewer_keywords: ["EC_SUBSCRIPTION_TYPE","EC_SUBSCRIPTION_TYPE enumeration","EcSubscriptionTypeCollectorInitiated","EcSubscriptionTypeSourceInitiated","evcoll/EC_SUBSCRIPTION_TYPE","evcoll/EcSubscriptionTypeCollectorInitiated","evcoll/EcSubscriptionTypeSourceInitiated","wec.ec_subscription_type","wes.ec_subscription_type"]
old-location: wec\ec_subscription_type.htm
tech.root: WEC
ms.assetid: b9906fd8-10d4-4bdd-97b9-fb1ae9d4c588
ms.date: 12/05/2018
ms.keywords: EC_SUBSCRIPTION_TYPE, EC_SUBSCRIPTION_TYPE enumeration, EcSubscriptionTypeCollectorInitiated, EcSubscriptionTypeSourceInitiated, evcoll/EC_SUBSCRIPTION_TYPE, evcoll/EcSubscriptionTypeCollectorInitiated, evcoll/EcSubscriptionTypeSourceInitiated, wec.ec_subscription_type, wes.ec_subscription_type
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EC_SUBSCRIPTION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EC_SUBSCRIPTION_TYPE
 - evcoll/_EC_SUBSCRIPTION_TYPE
 - EC_SUBSCRIPTION_TYPE
 - evcoll/EC_SUBSCRIPTION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_SUBSCRIPTION_TYPE
---

# EC_SUBSCRIPTION_TYPE enumeration


## -description

The <b>EC_SUBSCRIPTION_TYPE</b> enumeration specifies the type of subscription to use (a source initiated or collector initiated subscription).

## -enum-fields

### -field EcSubscriptionTypeSourceInitiated:0

Allows you to define an event subscription on an event collector computer without defining the event source computers. Multiple remote event source computers can then be set up (using a group policy setting) to forward events to the event collector computer. For more information, see <a href="/windows/desktop/WEC/setting-up-a-source-initiated-subscription">Setting up a Source Initiated Subscription</a>. This subscription type is useful when you do not know or you do not want to specify  all the event sources computers that will forward events.

### -field EcSubscriptionTypeCollectorInitiated:1

The computer that receives forwarded events from event sources (other computers that the events were published on) initiates the subscription. You specify all the event sources at the time the subscription is created.
