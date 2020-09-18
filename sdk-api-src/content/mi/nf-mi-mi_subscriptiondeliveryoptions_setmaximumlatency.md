---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetMaximumLatency
title: MI_SubscriptionDeliveryOptions_SetMaximumLatency function (mi.h)
description: Sets the maximum amount of time that the server will hold a result before delivering it to the client.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_SetMaximumLatency","MI_SubscriptionDeliveryOptions_SetMaximumLatency function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_SetMaximumLatency","wmi_v2.mi_subscriptiondeliveryoptions_setmaximumlatency"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setmaximumlatency.htm
tech.root: wmi_v2
ms.assetid: d28f4add-0f1c-4a9d-be0a-d91b1c8d9fc4
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetMaximumLatency, MI_SubscriptionDeliveryOptions_SetMaximumLatency function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetMaximumLatency, wmi_v2.mi_subscriptiondeliveryoptions_setmaximumlatency
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
 - MI_SubscriptionDeliveryOptions_SetMaximumLatency
 - mi/MI_SubscriptionDeliveryOptions_SetMaximumLatency
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
 - MI_SubscriptionDeliveryOptions_SetMaximumLatency
---

# MI_SubscriptionDeliveryOptions_SetMaximumLatency function


## -description

Sets the maximum amount of time that the server will hold a result before delivering it to the client.

## -parameters

### -param self [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value [in]

Latency value.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_interval">MI_Interval</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getmaximumlatency">MI_SubscriptionDeliveryOptions_GetMaximumLatency</a>