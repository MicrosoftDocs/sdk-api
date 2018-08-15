---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval
title: MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval function
author: windows-sdk-content
description: Gets the delivery retry interval&#8212;the amount of time to wait before retrying the delivery.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getdeliveryretryinterval.htm
old-project: wmi_v2
ms.assetid: 74ece97b-edf9-43f9-9afb-bb946ce13e89
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval, MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval, wmi_v2.mi_subscriptiondeliveryoptions_getdeliveryretryinterval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval function


## -description


Gets the delivery retry interval—the amount of time to wait before retrying the delivery.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure


### -param value [out]

Returned delivery retry interval.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



