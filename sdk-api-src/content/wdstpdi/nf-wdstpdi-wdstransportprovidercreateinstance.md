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

# WdsTransportProviderCreateInstance function


## -description


Opens a new instance of a content provider.


## -parameters




### -param pwszConfigString [in]

Configuration information for this instance of the content provider.


### -param phInstance [out]

Receives a pointer to a handle that identifies this instance.  When the instance is no longer needed, the handle should be closed with the <a href="https://msdn.microsoft.com/3eb0a931-ca5d-4db4-9c40-9c52f98be429">WdsTransportProviderCloseInstance</a> callback. 


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



