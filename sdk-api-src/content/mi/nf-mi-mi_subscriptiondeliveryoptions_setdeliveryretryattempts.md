---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts
title: MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts function (mi.h)
description: Sets the number of times a push delivery subscription will try to deliver a result.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts","MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts","wmi_v2.mi_subscriptiondeliveryoptions_setdeliveryretryattempts"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setdeliveryretryattempts.htm
tech.root: wmi_v2
ms.assetid: d00e94bc-83c7-4cb6-869d-c6e7c02c678c
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts, MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts, wmi_v2.mi_subscriptiondeliveryoptions_setdeliveryretryattempts
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
 - MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts
 - mi/MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts
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
 - MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts
---

# MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts function


## -description

Sets the number of times a push delivery subscription will try to deliver a result.

## -parameters

### -param self [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value [in]

Number of retry attempts for a failed push delivery.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliverydestination">MI_SubscriptionDeliveryOptions_GetDeliveryDestination</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryportnumber">MI_SubscriptionDeliveryOptions_GetDeliveryPortNumber</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryattempts">MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryinterval">MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliverydestination">MI_SubscriptionDeliveryOptions_SetDeliveryDestination</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryportnumber">MI_SubscriptionDeliveryOptions_SetDeliveryPortNumber</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryinterval">MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval</a>