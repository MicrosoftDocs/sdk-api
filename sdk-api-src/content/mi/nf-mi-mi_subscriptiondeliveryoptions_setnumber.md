---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetNumber
title: MI_SubscriptionDeliveryOptions_SetNumber function
author: windows-sdk-content
description: Sets the value of a named numeric option that is not covered by a dedicated function.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setnumber.htm
tech.root: wmi_v2
ms.assetid: 872af4f8-67e2-4e41-a629-180172dbdd17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_SubscriptionDeliveryOptions_SetNumber, MI_SubscriptionDeliveryOptions_SetNumber function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetNumber, wmi_v2.mi_subscriptiondeliveryoptions_setnumber
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
 - MI_SubscriptionDeliveryOptions_SetNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_SubscriptionDeliveryOptions_SetNumber function


## -description


Sets the value of a named numeric option that is not covered by a dedicated function.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option.


### -param value [in]

Option value.


### -param flags

Option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/80314490-204d-4b99-937f-f9b55266ac1a">MI_SubscriptionDeliveryOptions_GetNumber</a>
 

 

