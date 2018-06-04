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

# EcRetrySubscription function


## -description


The <b>EcRetrySubscription</b> function is used to retry connecting to the event source of a subscription that is not connected.


## -parameters




### -param SubscriptionName [in]

The name of the subscription to which to connect.


### -param EventSourceName [in]

The name of the event source of the subscription. This parameter is optional and can be <b>NULL</b>. This parameter must be <b>NULL</b> when the subscription is source initiated.  If this parameter is <b>NULL</b>, the entire subscription will be retried.


### -param Flags [in]

Reserved. Must be <b>NULL</b>.


## -returns



This function returns BOOL.




## -remarks



To retry a subscription for all the event sources of a subscription, use the <a href="https://msdn.microsoft.com/41702fb8-5b39-4daa-8904-aa36de18665c">EcSaveSubscription</a> function instead of calling <b>EcRetrySubscription</b> on each event source individually.


#### Examples

For example code using the <b>EcRetrySubscription</b> function, see <a href="https://msdn.microsoft.com/8a3570af-bde3-40e5-8129-84ec313d853f">Retrying an Event Collector Subscription</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

