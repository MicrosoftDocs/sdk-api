---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetNumber
title: MI_SubscriptionDeliveryOptions_GetNumber function
author: windows-driver-content
description: Gets the value of the named numeric option.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getnumber.htm
old-project: wmi_v2
ms.assetid: 80314490-204d-4b99-937f-f9b55266ac1a
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetNumber, MI_SubscriptionDeliveryOptions_GetNumber function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetNumber, wmi_v2.mi_subscriptiondeliveryoptions_getnumber
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
-	MI_SubscriptionDeliveryOptions_GetNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_GetNumber function


## -description


Gets the value of the named  numeric option.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option.


### -param value [out]

Returned option value.


### -param index [out, optional]

Returned zero-based index of the option.


### -param flags [out, optional]

Returned option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/872af4f8-67e2-4e41-a629-180172dbdd17">MI_SubscriptionDeliveryOptions_SetNumber</a>
 

 

