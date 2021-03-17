---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetInterval
title: MI_SubscriptionDeliveryOptions_GetInterval function (mi.h)
description: Gets the delivery interval for a specified option.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_GetInterval","MI_SubscriptionDeliveryOptions_GetInterval function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_GetInterval","wmi_v2.mi_subscriptiondeliveryoptions_getinterval"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getinterval.htm
tech.root: wmi_v2
ms.assetid: f515bfbf-2f28-4ee0-8f60-8725206b3568
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetInterval, MI_SubscriptionDeliveryOptions_GetInterval function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetInterval, wmi_v2.mi_subscriptiondeliveryoptions_getinterval
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
 - MI_SubscriptionDeliveryOptions_GetInterval
 - mi/MI_SubscriptionDeliveryOptions_GetInterval
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
 - MI_SubscriptionDeliveryOptions_GetInterval
---

# MI_SubscriptionDeliveryOptions_GetInterval function


## -description

Gets the delivery interval for a specified option.

## -parameters

### -param self [in]

A <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param optionName

A null-terminated string that represents the name of the option.

### -param value [out]

Returned interval.

### -param index [out, optional]

Returned zero-based index of option.

### -param flags [out, optional]

Returned option flags.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setinterval">MI_SubscriptionDeliveryOptions_SetInterval</a>