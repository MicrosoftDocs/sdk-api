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

# PathToRegion function


## -description


The <b>PathToRegion</b> function creates a region from the path that is selected into the specified device context. The resulting region uses device coordinates.


## -parameters




### -param hdc [in]

Handle to a device context that contains a closed path.


## -returns



If the function succeeds, the return value identifies a valid region.

If the function fails, the return value is zero.




## -remarks



When you no longer need the <b>HRGN</b> object call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

The device context identified by the <i>hdc</i> parameter must contain a closed path.

After <b>PathToRegion</b> converts a path into a region, the system discards the closed path from the specified device context.



