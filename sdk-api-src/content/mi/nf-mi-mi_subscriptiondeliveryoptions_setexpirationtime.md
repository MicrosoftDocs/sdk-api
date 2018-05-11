---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetExpirationTime
title: MI_SubscriptionDeliveryOptions_SetExpirationTime function
author: windows-driver-content
description: Sets the subscription expiration time (when the subscription will shut down).
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setexpirationtime.htm
old-project: wmi_v2
ms.assetid: c5cae015-7958-463b-9e44-a0452e366a14
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetExpirationTime, MI_SubscriptionDeliveryOptions_SetExpirationTime function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetExpirationTime, wmi_v2.mi_subscriptiondeliveryoptions_setexpirationtime
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
-	MI_SubscriptionDeliveryOptions_SetExpirationTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_SetExpirationTime function


## -description


Sets the subscription expiration time (when the subscription will shut down).


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param value [in]

Expiration time of the subscription.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/2f7d857f-5115-40a2-84d9-a4429d935de1">MI_Datetime</a>



<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/b76abb3b-e7f4-4b4b-866a-51a7d8b0066d">MI_SubscriptionDeliveryOptions_GetExpirationTime</a>
 

 

