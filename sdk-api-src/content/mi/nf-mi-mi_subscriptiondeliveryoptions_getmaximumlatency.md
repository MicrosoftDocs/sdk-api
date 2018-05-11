---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetMaximumLatency
title: MI_SubscriptionDeliveryOptions_GetMaximumLatency function
author: windows-driver-content
description: Gets the maximum amount of time that the server will hold a result before delivering it to the client.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getmaximumlatency.htm
old-project: wmi_v2
ms.assetid: 899fa8d5-0d39-44ea-994b-b13d4dc9b117
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetMaximumLatency, MI_SubscriptionDeliveryOptions_GetMaximumLatency function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetMaximumLatency, wmi_v2.mi_subscriptiondeliveryoptions_getmaximumlatency
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
-	MI_SubscriptionDeliveryOptions_GetMaximumLatency
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_GetMaximumLatency function


## -description


Gets the maximum amount of time that the server will hold a result before delivering it to the client.


## -parameters




### -param self [in]

A <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param value [out]

Returned latency value.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/b6bf3d47-c292-4140-8bc6-f15ad8a8019f">MI_Interval</a>



<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/d28f4add-0f1c-4a9d-be0a-d91b1c8d9fc4">MI_SubscriptionDeliveryOptions_SetMaximumLatency</a>
 

 

