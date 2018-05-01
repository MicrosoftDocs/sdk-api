---
UID: NF:mi.MI_SubscriptionDeliveryOptions_Clone
title: MI_SubscriptionDeliveryOptions_Clone function
author: windows-driver-content
description: Creates a copy of a MI_SubscriptionDeliveryOptions structure.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_clone.htm
old-project: wmi_v2
ms.assetid: 34374907-bbb6-4d22-81ac-2d662efaf119
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_SubscriptionDeliveryOptions_Clone, MI_SubscriptionDeliveryOptions_Clone function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_Clone, wmi_v2.mi_subscriptiondeliveryoptions_clone
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
-	MI_SubscriptionDeliveryOptions_Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_Clone function


## -description


Creates a copy of a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure to be cloned.


### -param newSubscriptionDeliveryOptions [out]

Returned <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> clone. This clone will eventually need to be deleted by calling the <a href="https://msdn.microsoft.com/658dcb26-4ba1-42ef-a404-b431d0c92864">MI_SubscriptionDeliveryOptions_Delete</a> function.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -see-also




<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/658dcb26-4ba1-42ef-a404-b431d0c92864">MI_SubscriptionDeliveryOptions_Delete</a>
 

 

