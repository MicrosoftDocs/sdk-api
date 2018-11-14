---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetDateTime
title: MI_SubscriptionDeliveryOptions_GetDateTime function
author: windows-sdk-content
description: Gets a previously set datetime option.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getdatetime.htm
tech.root: WMI_v2
ms.assetid: 502738a3-1f4a-460c-bd1c-5f1ea411d899
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetDateTime, MI_SubscriptionDeliveryOptions_GetDateTime function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetDateTime, wmi_v2.mi_subscriptiondeliveryoptions_getdatetime
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
 - MI_SubscriptionDeliveryOptions_GetDateTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_SubscriptionDeliveryOptions_GetDateTime
: 
---

# MI_SubscriptionDeliveryOptions_GetDateTime function


## -description


Gets a previously set datetime option.


## -parameters




### -param self [in]

A <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option to get.


### -param value [out]

Returned option value.


### -param index [out, optional]

Returned zero-based index of option.


### -param flags [out, optional]

Returned option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/2f7d857f-5115-40a2-84d9-a4429d935de1">MI_Datetime</a>



<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/d6f2820e-19f2-42b9-876b-4ceb09ea2db5">MI_SubscriptionDeliveryOptions_SetDateTime</a>
 

 

