---
UID: NE:evcoll._EC_SUBSCRIPTION_DELIVERY_MODE
title: EC_SUBSCRIPTION_DELIVERY_MODE (evcoll.h)
author: windows-sdk-content
description: Defines values that indicate how events are delivered in a subscription.
old-location: wec\ec_subscription_delivery_mode.htm
tech.root: WEC
ms.assetid: ece884d6-df3c-44d0-a10c-affcf3107148
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EC_SUBSCRIPTION_DELIVERY_MODE, EC_SUBSCRIPTION_DELIVERY_MODE enumeration, EcDeliveryModePull, EcDeliveryModePush, evcoll/EC_SUBSCRIPTION_DELIVERY_MODE, evcoll/EcDeliveryModePull, evcoll/EcDeliveryModePush, wec.ec_subscription_delivery_mode, wes.ec_subscription_delivery_mode
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_SUBSCRIPTION_DELIVERY_MODE
product: Windows
targetos: Windows
req.typenames: EC_SUBSCRIPTION_DELIVERY_MODE
req.redist: 
ms.custom: 19H1
---

# EC_SUBSCRIPTION_DELIVERY_MODE enumeration


## -description


The <b>EC_SUBSCRIPTION_DELIVERY_MODE</b> enumeration defines values that indicate how events are delivered in a  subscription. Events are delivered through subscriptions using either the push or pull model. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WES/subscribing-to-events">Subscribing to Events</a>.


## -enum-fields




### -field EcDeliveryModePull

Events are delivered through the subscription using the pull model.


### -field EcDeliveryModePush

Events are delivered through the subscription using the push model.

