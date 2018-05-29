---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetInterval
title: MI_SubscriptionDeliveryOptions_SetInterval function
author: windows-sdk-content
description: Sets the value of a named interval option.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setinterval.htm
old-project: wmi_v2
ms.assetid: 00b6dcbb-be09-464e-af7e-45dac4d70286
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetInterval, MI_SubscriptionDeliveryOptions_SetInterval function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetInterval, wmi_v2.mi_subscriptiondeliveryoptions_setinterval
ms.prod: windows
ms.technology: windows-sdk
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
-	MI_SubscriptionDeliveryOptions_SetInterval
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_SetInterval function


## -description


Sets the value of a named interval option.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option to set.


### -param value [in]

New value for the option.


### -param flags

Option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function is used to set interval options that are not covered by other dedicated functions containing the MI_SubscriptionDeliveryOptions_ prefix.




## -see-also




<a href="https://msdn.microsoft.com/b6bf3d47-c292-4140-8bc6-f15ad8a8019f">MI_Interval</a>



<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/f515bfbf-2f28-4ee0-8f60-8725206b3568">MI_SubscriptionDeliveryOptions_GetInterval</a>
 

 

