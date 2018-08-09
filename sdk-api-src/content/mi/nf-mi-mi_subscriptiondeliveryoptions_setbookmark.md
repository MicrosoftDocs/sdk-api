---
UID: NF:mi.MI_SubscriptionDeliveryOptions_SetBookmark
title: MI_SubscriptionDeliveryOptions_SetBookmark function
author: windows-sdk-content
description: Sets a bookmark for subscription indication delivery.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_setbookmark.htm
old-project: wmi_v2
ms.assetid: 9450dde9-fcd6-41c9-a1cb-2dce308653b8
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_SUBSCRIBE_BOOKMARK_NEWEST, MI_SUBSCRIBE_BOOKMARK_OLDEST, MI_SubscriptionDeliveryOptions_SetBookmark, MI_SubscriptionDeliveryOptions_SetBookmark function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_SetBookmark, wmi_v2.mi_subscriptiondeliveryoptions_setbookmark
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
 - MI_SubscriptionDeliveryOptions_SetBookmark
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_SetBookmark function


## -description


Sets a bookmark for subscription indication delivery.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param value

A null-terminated string that represents the bookmark that was retrieved from a previous indication result delivery, or one of two constants (<b>MI_SUBSCRIBE_BOOKMARK_OLDEST</b> or <b>MI_SUBSCRIBE_BOOKMARK_NEWEST</b>) that specify when a subscription should start.



#### MI_SUBSCRIBE_BOOKMARK_OLDEST (L"MI_SUBSCRIBE_BOOKMARK_OLDEST")

Start the subscription from the earliest possible indication.



#### MI_SUBSCRIBE_BOOKMARK_NEWEST (L"MI_SUBSCRIBE_BOOKMARK_NEWEST")

Start the subscription from this point.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function tells the server that bookmarks are required, and (if supported) it should return bookmarks with the indication results.




## -see-also




<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>



<a href="https://msdn.microsoft.com/f3c8721f-2aa0-40ca-ac51-3db03f9c5c30">MI_SubscriptionDeliveryOptions_GetBookmark</a>
 

 

