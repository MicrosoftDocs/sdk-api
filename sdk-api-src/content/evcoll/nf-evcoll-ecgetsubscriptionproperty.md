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

# EcGetSubscriptionProperty function


## -description


The <b>EcGetSubscriptionProperty</b> function retrieves a specific property value from a subscription object. The subscription object is specified by the handle passed into the <i>Subscription</i> parameter.


## -parameters




### -param Subscription [in]

The handle to the subscription object.


### -param PropertyId [in]

An identifier that specifies which property of the subscription to get. Specify a value from the <a href="https://msdn.microsoft.com/c70dca98-1c14-4c0c-9f2e-6241c463fe4e">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration. If you specify the <b>EcSubscriptionEventSources</b> value, then a handle to an array (<a href="https://msdn.microsoft.com/b78bdaf8-e034-40fe-acf8-632313e4fd94">EC_OBJECT_ARRAY_PROPERTY_HANDLE</a>) will be returned. You can then use the <a href="https://msdn.microsoft.com/a145c982-a1df-442f-8923-58f1db67ac25">EcGetObjectArrayProperty</a> and <a href="https://msdn.microsoft.com/0c219e3b-a7dd-4a7f-8fb3-0d281351ba24">EcSetObjectArrayProperty</a>  functions to get and set the Address, Enabled, UserName, and Password properties in the array.


### -param Flags [in]

Reserved. Must be <b>NULL</b>.


### -param PropertyValueBufferSize [in]

The size of the user-supplied buffer to store the property value into.


### -param PropertyValueBuffer [in]

The user-supplied buffer to store property value into.


### -param PropertyValueBufferUsed [out]

The size of the user-supplied buffer that is used by the function on successful return, or the size that is necessary to store the property value when function fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

