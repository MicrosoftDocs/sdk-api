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

# EcGetObjectArrayProperty function


## -description


The <b>EcGetObjectArrayProperty</b> function retrieves  property values from a handle to an array of event source properties. The array contains property values for the event sources of a subscription.


## -parameters




### -param ObjectArray [in]

A handle to an array of properties for the event sources for a subscription. An  array handle that is returned by the <a href="https://msdn.microsoft.com/984d986d-1c59-4d0c-88f3-40c66ffe43dd">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>PropertyId</i> parameter.


### -param PropertyId [in]

The property identifier for properties in the array. Specify a value from the <a href="https://msdn.microsoft.com/c70dca98-1c14-4c0c-9f2e-6241c463fe4e">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration. Get  the <b>Address</b>, <b>Enabled</b>, <b>UserName</b>, and <b>Password</b> properties in the array by specifying the <b>EcSubscriptionEventSourceAddress</b>, <b>EcSubscriptionEventSourceEnabled</b>, <b>EcSubscriptionEventSourceUserName</b>, or <b>EcSubscriptionEventSourcePassword</b> values.


### -param ArrayIndex [in]

The index of the array that specifies which event source to get the property from.


### -param Flags [in]

Reserved. Must be 0.


### -param PropertyValueBufferSize [in]

The size of the buffer that contains the value of the property. The size must be at least the size of an <a href="https://msdn.microsoft.com/f1f20e33-46b0-458e-ac6c-f890be20c455">EC_VARIANT</a> value.


### -param PropertyValueBuffer [in]

The user-supplied buffer to store property value into.


### -param PropertyValueBufferUsed [out]

The size of the user-supplied buffer that is used by the function on successful return, or the size that is necessary to store the property value when the function fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.


## -returns



This function returns BOOL.




## -remarks



Arrays are zero-based, so the index for the first item in the array is 0.

The Password property for an event source or the subscription cannot be retrieved. For security reasons, an empty string is returned for the property value and the last error will be set to <b>ERROR_ACCESS_DENIED</b>.

A subscription can have multiple event sources, and each source can have an <b>Address</b>, <b>Enabled</b>, <b>UserName</b>, and <b>Password</b> property.


#### Examples

For example code using the <b>EcGetObjectArrayProperty</b> function, see <a href="https://msdn.microsoft.com/984e21cf-3671-4aca-9e8e-bcad1fa2f02c">Displaying the Properties of an Event Collector Subscription</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

