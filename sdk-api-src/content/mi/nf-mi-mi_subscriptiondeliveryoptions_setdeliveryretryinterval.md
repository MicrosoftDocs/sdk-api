---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval
title: MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval function (mi.h)
description: Sets the delivery retry interval for subscriptions that are for push delivery.helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval","MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval","wmi_v2.mi_subscriptiondeliveryoptions_setdeliveryretryinterval"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setdeliveryretryinterval.htm
tech.root: wmi_v2
ms.assetid: 2abd46ad-c4a7-4e73-8b7d-2d9fecd10799
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval, MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval, wmi_v2.mi_subscriptiondeliveryoptions_setdeliveryretryinterval
f1_keywords:
- mi/MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mi.h
api_name:
- MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval function


## -description


Sets the delivery retry interval for subscriptions that are for push delivery.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.


### -param value [in]

Retry interval when attempting to delivery events via push delivery.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliverydestination">MI_SubscriptionDeliveryOptions_GetDeliveryDestination</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryportnumber">MI_SubscriptionDeliveryOptions_GetDeliveryPortNumber</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryattempts">MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryinterval">MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliverydestination">MI_SubscriptionDeliveryOptions_SetDeliveryDestination</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryportnumber">MI_SubscriptionDeliveryOptions_SetDeliveryPortNumber</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryattempts">MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts</a>
 

 

