---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetDeliveryDestination
title: MI_SubscriptionDeliveryOptions_SetDeliveryDestination function (mi.h)
description: Sets the destination endpoint that an indication will be delivered to.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_SetDeliveryDestination","MI_SubscriptionDeliveryOptions_SetDeliveryDestination function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_SetDeliveryDestination","wmi_v2.mi_subscriptiondeliveryoptions_setdeliverydestination"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setdeliverydestination.htm
tech.root: wmi_v2
ms.assetid: 01405c64-83ab-4c39-975c-7786659e2c18
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetDeliveryDestination, MI_SubscriptionDeliveryOptions_SetDeliveryDestination function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetDeliveryDestination, wmi_v2.mi_subscriptiondeliveryoptions_setdeliverydestination
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_SubscriptionDeliveryOptions_SetDeliveryDestination
 - mi/MI_SubscriptionDeliveryOptions_SetDeliveryDestination
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
 - MI_SubscriptionDeliveryOptions_SetDeliveryDestination
---

# MI_SubscriptionDeliveryOptions_SetDeliveryDestination function


## -description

Sets the destination endpoint that an indication will be delivered to.

## -parameters

### -param self [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value

A null-terminated string that represents the destination endpoint (machine name) to which to send the indication.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

This function is relevant only to push delivery.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliverydestination">MI_SubscriptionDeliveryOptions_GetDeliveryDestination</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryportnumber">MI_SubscriptionDeliveryOptions_GetDeliveryPortNumber</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryattempts">MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryinterval">MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryportnumber">MI_SubscriptionDeliveryOptions_SetDeliveryPortNumber</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryattempts">MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryinterval">MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval</a>