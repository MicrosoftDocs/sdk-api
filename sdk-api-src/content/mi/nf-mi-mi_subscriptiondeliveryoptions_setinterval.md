---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetInterval
title: MI_SubscriptionDeliveryOptions_SetInterval function (mi.h)
description: Sets the value of a named interval option.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_SetInterval","MI_SubscriptionDeliveryOptions_SetInterval function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_SetInterval","wmi_v2.mi_subscriptiondeliveryoptions_setinterval"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setinterval.htm
tech.root: wmi_v2
ms.assetid: 00b6dcbb-be09-464e-af7e-45dac4d70286
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetInterval, MI_SubscriptionDeliveryOptions_SetInterval function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetInterval, wmi_v2.mi_subscriptiondeliveryoptions_setinterval
f1_keywords:
- mi/MI_SubscriptionDeliveryOptions_SetInterval
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
- MI_SubscriptionDeliveryOptions_SetInterval
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_SubscriptionDeliveryOptions_SetInterval function


## -description


Sets the value of a named interval option.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option to set.


### -param value [in]

New value for the option.


### -param flags

Option flags.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function is used to set interval options that are not covered by other dedicated functions containing the MI_SubscriptionDeliveryOptions_ prefix.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_interval">MI_Interval</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getinterval">MI_SubscriptionDeliveryOptions_GetInterval</a>
 

 

