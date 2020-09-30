---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetBookmark
title: MI_SubscriptionDeliveryOptions_SetBookmark function (mi.h)
description: Sets a bookmark for subscription indication delivery.
helpviewer_keywords: ["MI_SUBSCRIBE_BOOKMARK_NEWEST","MI_SUBSCRIBE_BOOKMARK_OLDEST","MI_SubscriptionDeliveryOptions_SetBookmark","MI_SubscriptionDeliveryOptions_SetBookmark function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_SetBookmark","wmi_v2.mi_subscriptiondeliveryoptions_setbookmark"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setbookmark.htm
tech.root: wmi_v2
ms.assetid: 9450dde9-fcd6-41c9-a1cb-2dce308653b8
ms.date: 12/05/2018
ms.keywords: MI_SUBSCRIBE_BOOKMARK_NEWEST, MI_SUBSCRIBE_BOOKMARK_OLDEST, MI_SubscriptionDeliveryOptions_SetBookmark, MI_SubscriptionDeliveryOptions_SetBookmark function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetBookmark, wmi_v2.mi_subscriptiondeliveryoptions_setbookmark
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
 - MI_SubscriptionDeliveryOptions_SetBookmark
 - mi/MI_SubscriptionDeliveryOptions_SetBookmark
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
 - MI_SubscriptionDeliveryOptions_SetBookmark
---

# MI_SubscriptionDeliveryOptions_SetBookmark function


## -description

Sets a bookmark for subscription indication delivery.

## -parameters

### -param self [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value

A null-terminated string that represents the bookmark that was retrieved from a previous indication result delivery, or one of two constants (<b>MI_SUBSCRIBE_BOOKMARK_OLDEST</b> or <b>MI_SUBSCRIBE_BOOKMARK_NEWEST</b>) that specify when a subscription should start.



#### MI_SUBSCRIBE_BOOKMARK_OLDEST (L"MI_SUBSCRIBE_BOOKMARK_OLDEST")

Start the subscription from the earliest possible indication.



#### MI_SUBSCRIBE_BOOKMARK_NEWEST (L"MI_SUBSCRIBE_BOOKMARK_NEWEST")

Start the subscription from this point.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

This function tells the server that bookmarks are required, and (if supported) it should return bookmarks with the indication results.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getbookmark">MI_SubscriptionDeliveryOptions_GetBookmark</a>