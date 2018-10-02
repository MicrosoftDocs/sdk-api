---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts
title: MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts function
author: windows-sdk-content
description: Gets the number of delivery retry attempts.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getdeliveryretryattempts.htm
tech.root: WMI_v2
ms.assetid: 76d47c6c-6fbe-4fc5-aa19-2db7bd8c06a0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts, MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts, wmi_v2.mi_subscriptiondeliveryoptions_getdeliveryretryattempts
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
 - MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts function


## -description


Gets the number of delivery retry attempts.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure


### -param value [out]

Returned number of retry attempts.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



