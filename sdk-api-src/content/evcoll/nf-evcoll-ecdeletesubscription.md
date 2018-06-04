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

# EcDeleteSubscription function


## -description


The <b>EcDeleteSubscription</b> function deletes  an existing subscription that is specified by the <i>SubscriptionName</i> parameter. 

The function fails if the security descriptor of the subscription does not permit delete access for the calling process. 

If the subscription is active at the moment this API is called, then the subscription is deactivated.


## -parameters




### -param SubscriptionName [in]

The subscription to be deleted.


### -param Flags [in]

Reserved, must be 0.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

