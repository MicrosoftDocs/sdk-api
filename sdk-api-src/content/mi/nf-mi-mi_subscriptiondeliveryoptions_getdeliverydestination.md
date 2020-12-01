---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetDeliveryDestination
title: MI_SubscriptionDeliveryOptions_GetDeliveryDestination function (mi.h)
description: Gets the previously set subscription delivery destination.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_GetDeliveryDestination","MI_SubscriptionDeliveryOptions_GetDeliveryDestination function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_GetDeliveryDestination","wmi_v2.mi_subscriptiondeliveryoptions_getdeliverydestination"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getdeliverydestination.htm
tech.root: wmi_v2
ms.assetid: ef5476e0-8538-4446-bb30-6b77153d5896
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetDeliveryDestination, MI_SubscriptionDeliveryOptions_GetDeliveryDestination function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetDeliveryDestination, wmi_v2.mi_subscriptiondeliveryoptions_getdeliverydestination
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
 - MI_SubscriptionDeliveryOptions_GetDeliveryDestination
 - mi/MI_SubscriptionDeliveryOptions_GetDeliveryDestination
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
 - MI_SubscriptionDeliveryOptions_GetDeliveryDestination
---

# MI_SubscriptionDeliveryOptions_GetDeliveryDestination function


## -description

Gets the previously set subscription delivery destination.

## -parameters

### -param self [in]

A <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value

A pointer to a null-terminated string containing the returned destination name. This name is owned by the specified <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure and is valid until that structure is deleted.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryportnumber">MI_SubscriptionDeliveryOptions_GetDeliveryPortNumber</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryattempts">MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryinterval">MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliverydestination">MI_SubscriptionDeliveryOptions_SetDeliveryDestination</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryportnumber">MI_SubscriptionDeliveryOptions_SetDeliveryPortNumber</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryattempts">MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryinterval">MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval</a>