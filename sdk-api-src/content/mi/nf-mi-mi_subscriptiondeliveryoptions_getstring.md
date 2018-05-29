---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetString
title: MI_SubscriptionDeliveryOptions_GetString function
author: windows-sdk-content
description: Gets the value of the named string option.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getstring.htm
old-project: wmi_v2
ms.assetid: 5adbbe2a-2cfa-4d24-97e8-5a5d02a685e3
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetString, MI_SubscriptionDeliveryOptions_GetString function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetString, wmi_v2.mi_subscriptiondeliveryoptions_getstring
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
-	MI_SubscriptionDeliveryOptions_GetString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_GetString function


## -description


Gets the value of the named string option.


## -parameters




### -param self [in]

A <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option.


### -param value

A pointer to a null-terminated string containing the returned option value.


### -param index [out, optional]

Returned zero-based index of option.


### -param flags [out, optional]

Returned option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/c2bcf5b7-24c1-43cd-bf65-18ad891be7b8">MI_SubscriptionDeliveryOptions_SetString</a>
 

 

