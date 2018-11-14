---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetMaximumLatency
title: MI_SubscriptionDeliveryOptions_SetMaximumLatency function
author: windows-sdk-content
description: Sets the maximum amount of time that the server will hold a result before delivering it to the client.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setmaximumlatency.htm
tech.root: WMI_v2
ms.assetid: d28f4add-0f1c-4a9d-be0a-d91b1c8d9fc4
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetMaximumLatency, MI_SubscriptionDeliveryOptions_SetMaximumLatency function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetMaximumLatency, wmi_v2.mi_subscriptiondeliveryoptions_setmaximumlatency
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
 - MI_SubscriptionDeliveryOptions_SetMaximumLatency
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_SubscriptionDeliveryOptions_SetMaximumLatency
: 
---

# MI_SubscriptionDeliveryOptions_SetMaximumLatency function


## -description


Sets the maximum amount of time that the server will hold a result before delivering it to the client.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param value [in]

Latency value.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/b6bf3d47-c292-4140-8bc6-f15ad8a8019f">MI_Interval</a>



<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/899fa8d5-0d39-44ea-994b-b13d4dc9b117">MI_SubscriptionDeliveryOptions_GetMaximumLatency</a>
 

 

