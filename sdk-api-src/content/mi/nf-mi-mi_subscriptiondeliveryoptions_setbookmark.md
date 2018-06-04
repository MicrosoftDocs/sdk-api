---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

