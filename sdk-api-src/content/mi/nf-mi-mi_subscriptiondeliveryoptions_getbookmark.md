---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetBookmark
title: MI_SubscriptionDeliveryOptions_GetBookmark function (mi.h)
description: Gets a previously set subscription bookmark.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_GetBookmark","MI_SubscriptionDeliveryOptions_GetBookmark function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_GetBookmark","wmi_v2.mi_subscriptiondeliveryoptions_getbookmark"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getbookmark.htm
tech.root: wmi_v2
ms.assetid: f3c8721f-2aa0-40ca-ac51-3db03f9c5c30
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetBookmark, MI_SubscriptionDeliveryOptions_GetBookmark function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetBookmark, wmi_v2.mi_subscriptiondeliveryoptions_getbookmark
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
 - MI_SubscriptionDeliveryOptions_GetBookmark
 - mi/MI_SubscriptionDeliveryOptions_GetBookmark
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
 - MI_SubscriptionDeliveryOptions_GetBookmark
---

# MI_SubscriptionDeliveryOptions_GetBookmark function


## -description

Gets a previously set subscription bookmark.

## -parameters

### -param self [in]

A <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value

A pointer to a null-terminated string containing the returned subscription bookmark. This value is owned by the <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure specified in the <i>self</i> parameter, so <i>value</i> does not need to be deleted. It is valid until the structure goes away.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setbookmark">MI_SubscriptionDeliveryOptions_SetBookmark</a>