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

# EcEnumNextSubscription function


## -description


The <b>EcEnumNextSubscription</b> function continues the enumeration of the subscriptions registered on the local machine.


## -parameters




### -param SubscriptionEnum [in]

The handle to the enumerator object that is returned from the <a href="https://msdn.microsoft.com/edbfabb0-6ad1-415a-a2ef-094b1d3bcccb">EcOpenSubscriptionEnum</a> function.


### -param SubscriptionNameBufferSize [in]

The size of the user-supplied buffer (in chars) to store the subscription name.


### -param SubscriptionNameBuffer [in]

The user-supplied buffer to store the subscription name.


### -param SubscriptionNameBufferUsed [out]

The size of the user-supplied buffer that is used by the function on successful return, or the size that is necessary to store the subscription name when the function fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

