---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetDateTime
title: MI_SubscriptionDeliveryOptions_SetDateTime function (mi.h)
description: Sets the value of a named DateTime option.helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_SetDateTime","MI_SubscriptionDeliveryOptions_SetDateTime function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_SetDateTime","wmi_v2.mi_subscriptiondeliveryoptions_setdatetime"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setdatetime.htm
tech.root: wmi_v2
ms.assetid: d6f2820e-19f2-42b9-876b-4ceb09ea2db5
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetDateTime, MI_SubscriptionDeliveryOptions_SetDateTime function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetDateTime, wmi_v2.mi_subscriptiondeliveryoptions_setdatetime
f1_keywords:
- mi/MI_SubscriptionDeliveryOptions_SetDateTime
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
- MI_SubscriptionDeliveryOptions_SetDateTime
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_SubscriptionDeliveryOptions_SetDateTime function


## -description


Sets the value of a named DateTime option.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.


### -param optionName [in]

A null-terminated string that represents the name of the option.


### -param value [in]

Option value.


### -param flags

Option flags.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_datetime">MI_Datetime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdatetime">MI_SubscriptionDeliveryOptions_GetDateTime</a>
 

 

