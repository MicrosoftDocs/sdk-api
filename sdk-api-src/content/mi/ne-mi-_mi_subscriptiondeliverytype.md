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

# _MI_SubscriptionDeliveryType enumeration


## -description


Differentiates between a push or pull subscription delivery type. This is not supported when using the DCOM protocol.


## -enum-fields




### -field MI_SubscriptionDeliveryType_Pull

Pull delivery is required for subscriptions. Pulling the indications from the server is more firewall friendly. However, it can also be slower than the push delivery type.


### -field MI_SubscriptionDeliveryType_Push

Push delivery is required for subscriptions. Push indicates that the server will connect to the client to deliver the event when one is available. This requires the firewall on the correct ports to work and security contexts need to managed carefully.

