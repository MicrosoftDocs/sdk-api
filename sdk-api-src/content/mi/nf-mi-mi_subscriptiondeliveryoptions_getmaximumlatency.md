---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetMaximumLatency
title: MI_SubscriptionDeliveryOptions_GetMaximumLatency function (mi.h)
description: Gets the maximum amount of time that the server will hold a result before delivering it to the client.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_GetMaximumLatency","MI_SubscriptionDeliveryOptions_GetMaximumLatency function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_GetMaximumLatency","wmi_v2.mi_subscriptiondeliveryoptions_getmaximumlatency"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getmaximumlatency.htm
tech.root: wmi_v2
ms.assetid: 899fa8d5-0d39-44ea-994b-b13d4dc9b117
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetMaximumLatency, MI_SubscriptionDeliveryOptions_GetMaximumLatency function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetMaximumLatency, wmi_v2.mi_subscriptiondeliveryoptions_getmaximumlatency
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
 - MI_SubscriptionDeliveryOptions_GetMaximumLatency
 - mi/MI_SubscriptionDeliveryOptions_GetMaximumLatency
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
 - MI_SubscriptionDeliveryOptions_GetMaximumLatency
---

# MI_SubscriptionDeliveryOptions_GetMaximumLatency function


## -description

Gets the maximum amount of time that the server will hold a result before delivering it to the client.

## -parameters

### -param self [in]

A <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value [out]

Returned latency value.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_interval">MI_Interval</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setmaximumlatency">MI_SubscriptionDeliveryOptions_SetMaximumLatency</a>