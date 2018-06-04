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

# EcSetSubscriptionProperty function


## -description


The <b>EcSetSubscriptionProperty</b> function sets new values or updates existing values of a subscription. New values set through this method will not be active unless they are saved by the <a href="https://msdn.microsoft.com/41702fb8-5b39-4daa-8904-aa36de18665c">EcSaveSubscription</a> method.


## -parameters




### -param Subscription [in]

The handle to the subscription object.


### -param PropertyId [in]

A value from the  <a href="https://msdn.microsoft.com/c70dca98-1c14-4c0c-9f2e-6241c463fe4e">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration that specifies which property of the subscription to set.


### -param Flags [in]

Reserved. Must be 0.


### -param PropertyValue [in]

The value of the property to set for the indicated subscription property.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

