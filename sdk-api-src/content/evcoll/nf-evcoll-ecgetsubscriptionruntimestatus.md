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

# EcGetSubscriptionRunTimeStatus function


## -description


The <b>EcGetSubscriptionRunTimeStatus</b> function retrieves the run time status information for an event source of a subscription or the subscription itself. The subscription is specified by its name. If the event source is <b>NULL</b>, then the status for the overall subscription is retrieved.


## -parameters




### -param SubscriptionName [in]

The name of the subscription to get the run time status information from.


### -param StatusInfoId [in]

An identifier that specifies which run time status information to get from the subscription. Specify a value from the <a href="https://msdn.microsoft.com/cc4e58d5-22cf-4823-be5d-e056f6690a45">EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID</a> enumeration. The <b>EcSubscriptionRunTimeStatusEventSources</b> value can be used to obtain the list of event sources associated with a subscription.


### -param EventSourceName [in]

The name of the event source to get the status from. Each subscription can have multiple event sources.


### -param Flags [in]

Reserved. Must be <b>NULL</b>.


### -param StatusValueBufferSize [in]

The size of the user-supplied buffer that will hold the run time status information.


### -param StatusValueBuffer [in]

The user-supplied buffer that will hold the run time status information. The buffer will hold the appropriate value depending on the <a href="https://msdn.microsoft.com/cc4e58d5-22cf-4823-be5d-e056f6690a45">EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID</a> value passed into the <i>StatusInfoId</i> parameter.


### -param StatusValueBufferUsed [out]

The size of the user supplied buffer that is used by the function on successful return, or the size that is necessary to store the property value when function fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

