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

# MI_Application_NewSubscriptionDeliveryOptions function


## -description


Creates an <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> object that represents the configuration needed to carry out subscribe operations over certain protocols.


## -parameters




### -param application [in]

A pointer to a handle returned from the <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a> function.


### -param deliveryType [in]

A value of the <a href="https://msdn.microsoft.com/3e1eb580-8f36-4ddb-8d65-7c7e65dd08bb">MI_SubscriptionDeliveryType</a> enumeration that specifies how the indications are delivered.


### -param deliveryOptions [out]

The returned <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> object.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



When you have finished using the returned <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> object, close it by calling the <a href="https://msdn.microsoft.com/658dcb26-4ba1-42ef-a404-b431d0c92864">MI_SubscriptionDeliveryOptions_Delete</a> function.



