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

# NetworkIsolationGetEnterpriseIdClose function


## -description


This API is used for closing the handle returned by  <a href="https://msdn.microsoft.com/709211F9-FE7A-4C43-AD35-101C4B64ED26">NetworkIsolationGetEnterpriseIdAsync</a> as well as for synchronizing the operation.


## -parameters




### -param hOperation [in]

The handle to release.


### -param bWaitForOperation [in]

Indicates whether to wait for synchronization.


## -returns



Returns ERROR_SUCCESS if successful, or an error value otherwise. 



