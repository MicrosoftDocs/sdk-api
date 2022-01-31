---
UID: NE:mi._MI_SubscriptionDeliveryType
title: MI_SubscriptionDeliveryType (mi.h)
description: Differentiates between a push or pull subscription delivery type. This is not supported when using the DCOM protocol.
helpviewer_keywords: ["MI_SubscriptionDeliveryType","MI_SubscriptionDeliveryType enumeration [Windows Management Infrastructure (MI)]","MI_SubscriptionDeliveryType_Pull","MI_SubscriptionDeliveryType_Push","mi/MI_SubscriptionDeliveryType","mi/MI_SubscriptionDeliveryType_Pull","mi/MI_SubscriptionDeliveryType_Push","wmi._mi_subscriptiondeliverytype","wmi_v2.mi_subscriptiondeliverytype"]
old-location: wmi_v2\mi_subscriptiondeliverytype.htm
tech.root: wmi_v2
ms.assetid: 3e1eb580-8f36-4ddb-8d65-7c7e65dd08bb
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryType, MI_SubscriptionDeliveryType enumeration [Windows Management Infrastructure (MI)], MI_SubscriptionDeliveryType_Pull, MI_SubscriptionDeliveryType_Push, mi/MI_SubscriptionDeliveryType, mi/MI_SubscriptionDeliveryType_Pull, mi/MI_SubscriptionDeliveryType_Push, wmi._mi_subscriptiondeliverytype, wmi_v2.mi_subscriptiondeliverytype
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_SubscriptionDeliveryType
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_SubscriptionDeliveryType
 - mi/_MI_SubscriptionDeliveryType
 - MI_SubscriptionDeliveryType
 - mi/MI_SubscriptionDeliveryType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_SubscriptionDeliveryType
---

# MI_SubscriptionDeliveryType enumeration


## -description

Differentiates between a push or pull subscription delivery type. This is not supported when using the DCOM protocol.

## -enum-fields

### -field MI_SubscriptionDeliveryType_Pull:1

Pull delivery is required for subscriptions. Pulling the indications from the server is more firewall friendly. However, it can also be slower than the push delivery type.

### -field MI_SubscriptionDeliveryType_Push:2

Push delivery is required for subscriptions. Push indicates that the server will connect to the client to deliver the event when one is available. This requires the firewall on the correct ports to work and security contexts need to managed carefully.

