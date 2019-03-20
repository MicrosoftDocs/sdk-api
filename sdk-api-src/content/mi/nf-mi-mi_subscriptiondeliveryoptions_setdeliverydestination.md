---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetDeliveryDestination
title: MI_SubscriptionDeliveryOptions_SetDeliveryDestination function (mi.h)
author: windows-sdk-content
description: Sets the destination endpoint that an indication will be delivered to.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setdeliverydestination.htm
tech.root: wmi_v2
ms.assetid: 01405c64-83ab-4c39-975c-7786659e2c18
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetDeliveryDestination, MI_SubscriptionDeliveryOptions_SetDeliveryDestination function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetDeliveryDestination, wmi_v2.mi_subscriptiondeliveryoptions_setdeliverydestination
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
 - MI_SubscriptionDeliveryOptions_SetDeliveryDestination
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_SubscriptionDeliveryOptions_SetDeliveryDestination function


## -description


Sets the destination endpoint that an indication will be delivered to.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param value

A null-terminated string that represents the destination endpoint (machine name) to which to send the indication.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



This function is relevant only to push delivery.




## -see-also




<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/ef5476e0-8538-4446-bb30-6b77153d5896">MI_SubscriptionDeliveryOptions_GetDeliveryDestination</a>



<a href="https://msdn.microsoft.com/8d3d86c1-6b95-4435-8821-7a0d58a4af5c">MI_SubscriptionDeliveryOptions_GetDeliveryPortNumber</a>



<a href="https://msdn.microsoft.com/76d47c6c-6fbe-4fc5-aa19-2db7bd8c06a0">MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts</a>



<a href="https://msdn.microsoft.com/74ece97b-edf9-43f9-9afb-bb946ce13e89">MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval</a>



<a href="https://msdn.microsoft.com/e5498e1a-d08b-421f-ba31-35b1378af871">MI_SubscriptionDeliveryOptions_SetDeliveryPortNumber</a>



<a href="https://msdn.microsoft.com/d00e94bc-83c7-4cb6-869d-c6e7c02c678c">MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts</a>



<a href="https://msdn.microsoft.com/2abd46ad-c4a7-4e73-8b7d-2d9fecd10799">MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval</a>
 

 

