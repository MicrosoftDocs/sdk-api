---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetHeartbeatInterval
title: MI_SubscriptionDeliveryOptions_SetHeartbeatInterval function
author: windows-driver-content
description: Sets the heartbeat interval.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setheartbeatinterval.htm
old-project: wmi_v2
ms.assetid: eb747c85-1ad1-4510-b674-7d9cf9fa9021
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetHeartbeatInterval, MI_SubscriptionDeliveryOptions_SetHeartbeatInterval function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetHeartbeatInterval, wmi_v2.mi_subscriptiondeliveryoptions_setheartbeatinterval
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
-	MI_SubscriptionDeliveryOptions_SetHeartbeatInterval
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_SetHeartbeatInterval function


## -description


Sets the heartbeat interval.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param value [in]

Interval between delivery of results whereby the server notifies the client that the server is still connected.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



If no events are available, the server uses this interval to send a heartbeat back to the client so that the client knows that the server is still there. This function is relevant for push delivery.




## -see-also




<a href="https://msdn.microsoft.com/b6bf3d47-c292-4140-8bc6-f15ad8a8019f">MI_Interval</a>



<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/ef5476e0-8538-4446-bb30-6b77153d5896">MI_SubscriptionDeliveryOptions_GetDeliveryDestination</a>



<a href="https://msdn.microsoft.com/8d3d86c1-6b95-4435-8821-7a0d58a4af5c">MI_SubscriptionDeliveryOptions_GetDeliveryPortNumber</a>



<a href="https://msdn.microsoft.com/76d47c6c-6fbe-4fc5-aa19-2db7bd8c06a0">MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts</a>



<a href="https://msdn.microsoft.com/74ece97b-edf9-43f9-9afb-bb946ce13e89">MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval</a>



<a href="https://msdn.microsoft.com/36d415f8-0bb9-4825-aa01-c42c5c91564f">MI_SubscriptionDeliveryOptions_GetHeartbeatInterval</a>



<a href="https://msdn.microsoft.com/01405c64-83ab-4c39-975c-7786659e2c18">MI_SubscriptionDeliveryOptions_SetDeliveryDestination</a>



<a href="https://msdn.microsoft.com/e5498e1a-d08b-421f-ba31-35b1378af871">MI_SubscriptionDeliveryOptions_SetDeliveryPortNumber</a>



<a href="https://msdn.microsoft.com/d00e94bc-83c7-4cb6-869d-c6e7c02c678c">MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts</a>



<a href="https://msdn.microsoft.com/2abd46ad-c4a7-4e73-8b7d-2d9fecd10799">MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval</a>
 

 

