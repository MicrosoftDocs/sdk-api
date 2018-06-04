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

# IEventSubscription::put_SubscriberCLSID


## -description


The CLSID of the subscriber component (for a persistent subscription).

This property is read/write.


## -parameters


## -remarks



If not empty, the subscription is persistent and the <a href="https://msdn.microsoft.com/207c8e74-d8f8-4576-8f2d-762c97bc048f">SubscriberInterface</a> property must be <b>NULL</b>. This property works in conjunction with the <a href="https://msdn.microsoft.com/b56027ac-abe6-4d13-ad3a-254a2f92ab6d">MachineName</a> property in a persistent subscription.




## -see-also




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>
 

 

