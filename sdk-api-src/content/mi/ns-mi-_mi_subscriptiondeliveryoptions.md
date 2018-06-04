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

# _MI_SubscriptionDeliveryOptions structure


## -description


The subscription options object stores configuration options used for passing into subscription operations.


## -struct-fields




### -field reserved1

Reserved for internal use only.


### -field reserved2

Reserved for internal use only.


### -field ft

Pointer to the <b>MI_SubscriptionDeliveryOptions</b> function table.


## -remarks



This structure is created by calling the <a href="https://msdn.microsoft.com/ac84ec09-7d91-42fc-8271-3e0e54bbb788">MI_Application_NewSubscriptionDeliveryOptions</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ac84ec09-7d91-42fc-8271-3e0e54bbb788">MI_Application_NewSubscriptionDeliveryOptions</a>
 

 

