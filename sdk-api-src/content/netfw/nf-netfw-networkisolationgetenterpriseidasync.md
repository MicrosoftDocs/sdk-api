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

# NetworkIsolationGetEnterpriseIdAsync function


## -description


Gets the Enterprise ID for Enterprise Data Protection Server endpoints.


## -parameters




### -param wszServerName [in]

The name of the Enterprise Data Protection Server.


### -param dwFlags [in]

Not implemented. Set to 0.


### -param context [in, optional]

Optional context pointer. 


### -param callback [in]

Function pointer that will be invoked when a notification is ready for delivery.


### -param hOperation [out]

The handle for the Enterprise Data Protection Server endpoints.


## -returns



Returns ERROR_SUCCESS if successful, or an error value otherwise. 



