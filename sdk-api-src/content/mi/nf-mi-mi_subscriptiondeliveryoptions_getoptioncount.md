---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetOptionCount
title: MI_SubscriptionDeliveryOptions_GetOptionCount function (mi.h)
description: Gets the number of previously set options.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_GetOptionCount","MI_SubscriptionDeliveryOptions_GetOptionCount function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_GetOptionCount","wmi_v2.mi_subscriptiondeliveryoptions_getoptioncount"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getoptioncount.htm
tech.root: wmi_v2
ms.assetid: 695a4ec8-4e6b-4a3d-800b-fa0edfab5ca2
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetOptionCount, MI_SubscriptionDeliveryOptions_GetOptionCount function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetOptionCount, wmi_v2.mi_subscriptiondeliveryoptions_getoptioncount
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
 - MI_SubscriptionDeliveryOptions_GetOptionCount
 - mi/MI_SubscriptionDeliveryOptions_GetOptionCount
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
 - MI_SubscriptionDeliveryOptions_GetOptionCount
---

# MI_SubscriptionDeliveryOptions_GetOptionCount function


## -description

Gets the number of previously set options.

## -parameters

### -param self [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure

### -param count [out, optional]

Returned number of previously set options.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.