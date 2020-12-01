---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetDateTime
title: MI_SubscriptionDeliveryOptions_GetDateTime function (mi.h)
description: Gets a previously set datetime option.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_GetDateTime","MI_SubscriptionDeliveryOptions_GetDateTime function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_GetDateTime","wmi_v2.mi_subscriptiondeliveryoptions_getdatetime"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getdatetime.htm
tech.root: wmi_v2
ms.assetid: 502738a3-1f4a-460c-bd1c-5f1ea411d899
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetDateTime, MI_SubscriptionDeliveryOptions_GetDateTime function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetDateTime, wmi_v2.mi_subscriptiondeliveryoptions_getdatetime
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_SubscriptionDeliveryOptions_GetDateTime
 - mi/MI_SubscriptionDeliveryOptions_GetDateTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_SubscriptionDeliveryOptions_GetDateTime
---

# MI_SubscriptionDeliveryOptions_GetDateTime function


## -description

Gets a previously set datetime option.

## -parameters

### -param self [in]

A <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param optionName

A null-terminated string that represents the name of the option to get.

### -param value [out]

Returned option value.

### -param index [out, optional]

Returned zero-based index of option.

### -param flags [out, optional]

Returned option flags.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_datetime">MI_Datetime</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdatetime">MI_SubscriptionDeliveryOptions_SetDateTime</a>