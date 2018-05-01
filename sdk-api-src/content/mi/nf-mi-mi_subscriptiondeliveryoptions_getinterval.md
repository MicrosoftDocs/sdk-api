---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetInterval
title: MI_SubscriptionDeliveryOptions_GetInterval function
author: windows-driver-content
description: Gets the delivery interval for a specified option.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getinterval.htm
old-project: wmi_v2
ms.assetid: f515bfbf-2f28-4ee0-8f60-8725206b3568
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetInterval, MI_SubscriptionDeliveryOptions_GetInterval function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetInterval, wmi_v2.mi_subscriptiondeliveryoptions_getinterval
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_SubscriptionDeliveryOptions_GetInterval
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_GetInterval function


## -description


Gets the delivery interval for a specified option.


## -parameters




### -param self [in]

A <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option.


### -param value [out]

Returned interval.


### -param index [out, optional]

Returned zero-based index of option.


### -param flags [out, optional]

Returned option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/00b6dcbb-be09-464e-af7e-45dac4d70286">MI_SubscriptionDeliveryOptions_SetInterval</a>
 

 

