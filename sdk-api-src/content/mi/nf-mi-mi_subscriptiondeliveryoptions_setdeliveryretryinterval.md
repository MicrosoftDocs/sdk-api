---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval function


## -description


Sets the delivery retry interval for subscriptions that are for push delivery.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param value [in]

Retry interval when attempting to delivery events via push delivery.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/ef5476e0-8538-4446-bb30-6b77153d5896">MI_SubscriptionDeliveryOptions_GetDeliveryDestination</a>



<a href="https://msdn.microsoft.com/8d3d86c1-6b95-4435-8821-7a0d58a4af5c">MI_SubscriptionDeliveryOptions_GetDeliveryPortNumber</a>



<a href="https://msdn.microsoft.com/76d47c6c-6fbe-4fc5-aa19-2db7bd8c06a0">MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts</a>



<a href="https://msdn.microsoft.com/74ece97b-edf9-43f9-9afb-bb946ce13e89">MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval</a>



<a href="https://msdn.microsoft.com/01405c64-83ab-4c39-975c-7786659e2c18">MI_SubscriptionDeliveryOptions_SetDeliveryDestination</a>



<a href="https://msdn.microsoft.com/e5498e1a-d08b-421f-ba31-35b1378af871">MI_SubscriptionDeliveryOptions_SetDeliveryPortNumber</a>



<a href="https://msdn.microsoft.com/d00e94bc-83c7-4cb6-869d-c6e7c02c678c">MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts</a>
 

 

