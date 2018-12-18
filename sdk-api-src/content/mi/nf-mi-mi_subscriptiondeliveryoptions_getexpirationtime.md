---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetExpirationTime
title: MI_SubscriptionDeliveryOptions_GetExpirationTime function
author: windows-sdk-content
description: Gets the delivery expiration value (which can be expressed as a timestamp or an interval).
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getexpirationtime.htm
tech.root: wmi_v2
ms.assetid: b76abb3b-e7f4-4b4b-866a-51a7d8b0066d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetExpirationTime, MI_SubscriptionDeliveryOptions_GetExpirationTime function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetExpirationTime, wmi_v2.mi_subscriptiondeliveryoptions_getexpirationtime
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
 - MI_SubscriptionDeliveryOptions_GetExpirationTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_SubscriptionDeliveryOptions_GetExpirationTime function


## -description


Gets the delivery expiration value (which can be expressed as a timestamp or an interval).


## -parameters




### -param self [in, out]

A <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param value [out]

Returned delivery expiration value. This value is a <a href="https://msdn.microsoft.com/2f7d857f-5115-40a2-84d9-a4429d935de1">MI_Datetime</a> structure that can contain either a timestamp or an interval.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/2f7d857f-5115-40a2-84d9-a4429d935de1">MI_Datetime</a>



<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/c5cae015-7958-463b-9e44-a0452e366a14">MI_SubscriptionDeliveryOptions_SetExpirationTime</a>
 

 

