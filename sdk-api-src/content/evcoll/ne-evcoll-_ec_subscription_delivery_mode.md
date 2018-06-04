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

# _EC_SUBSCRIPTION_DELIVERY_MODE enumeration


## -description


The <b>EC_SUBSCRIPTION_DELIVERY_MODE</b> enumeration defines values that indicate how events are delivered in a  subscription. Events are delivered through subscriptions using either the push or pull model. For more information, see <a href="https://msdn.microsoft.com/1e86deeb-fc59-4658-9353-e4ced7ace89a">Subscribing to Events</a>.


## -enum-fields




### -field EcDeliveryModePull

Events are delivered through the subscription using the pull model.


### -field EcDeliveryModePush

Events are delivered through the subscription using the push model.

