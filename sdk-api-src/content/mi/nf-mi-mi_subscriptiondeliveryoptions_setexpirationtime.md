---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetExpirationTime
title: MI_SubscriptionDeliveryOptions_SetExpirationTime function (mi.h)
description: Sets the subscription expiration time (when the subscription will shut down).
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_SetExpirationTime","MI_SubscriptionDeliveryOptions_SetExpirationTime function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_SetExpirationTime","wmi_v2.mi_subscriptiondeliveryoptions_setexpirationtime"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setexpirationtime.htm
tech.root: wmi_v2
ms.assetid: c5cae015-7958-463b-9e44-a0452e366a14
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetExpirationTime, MI_SubscriptionDeliveryOptions_SetExpirationTime function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetExpirationTime, wmi_v2.mi_subscriptiondeliveryoptions_setexpirationtime
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
 - MI_SubscriptionDeliveryOptions_SetExpirationTime
 - mi/MI_SubscriptionDeliveryOptions_SetExpirationTime
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
 - MI_SubscriptionDeliveryOptions_SetExpirationTime
---

# MI_SubscriptionDeliveryOptions_SetExpirationTime function


## -description

Sets the subscription expiration time (when the subscription will shut down).

## -parameters

### -param self [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value [in]

Expiration time of the subscription.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_datetime">MI_Datetime</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getexpirationtime">MI_SubscriptionDeliveryOptions_GetExpirationTime</a>