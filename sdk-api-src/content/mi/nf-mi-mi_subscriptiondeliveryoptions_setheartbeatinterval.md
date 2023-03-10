---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetHeartbeatInterval
title: MI_SubscriptionDeliveryOptions_SetHeartbeatInterval function (mi.h)
description: Sets the heartbeat interval.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_SetHeartbeatInterval","MI_SubscriptionDeliveryOptions_SetHeartbeatInterval function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_SetHeartbeatInterval","wmi_v2.mi_subscriptiondeliveryoptions_setheartbeatinterval"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setheartbeatinterval.htm
tech.root: wmi_v2
ms.assetid: eb747c85-1ad1-4510-b674-7d9cf9fa9021
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetHeartbeatInterval, MI_SubscriptionDeliveryOptions_SetHeartbeatInterval function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetHeartbeatInterval, wmi_v2.mi_subscriptiondeliveryoptions_setheartbeatinterval
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
 - MI_SubscriptionDeliveryOptions_SetHeartbeatInterval
 - mi/MI_SubscriptionDeliveryOptions_SetHeartbeatInterval
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
 - MI_SubscriptionDeliveryOptions_SetHeartbeatInterval
---

# MI_SubscriptionDeliveryOptions_SetHeartbeatInterval function


## -description

Sets the heartbeat interval.

## -parameters

### -param self [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value [in]

Interval between delivery of results whereby the server notifies the client that the server is still connected.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

If no events are available, the server uses this interval to send a heartbeat back to the client so that the client knows that the server is still there. This function is relevant for push delivery.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_interval">MI_Interval</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliverydestination">MI_SubscriptionDeliveryOptions_GetDeliveryDestination</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryportnumber">MI_SubscriptionDeliveryOptions_GetDeliveryPortNumber</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryattempts">MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryinterval">MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getheartbeatinterval">MI_SubscriptionDeliveryOptions_GetHeartbeatInterval</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliverydestination">MI_SubscriptionDeliveryOptions_SetDeliveryDestination</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryportnumber">MI_SubscriptionDeliveryOptions_SetDeliveryPortNumber</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryattempts">MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryinterval">MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval</a>