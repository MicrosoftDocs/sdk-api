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

# HasExpandedResources function


## -description


Gets the current resource state (that is, whether the app is running in Game Mode or shared mode).


## -parameters




### -param hasExpandedResources [out]

True if  the app is running in Game Mode; otherwise, false.


## -returns



The result of the operation.




## -remarks



This is a Win32 API that's supported in UWP desktop and Xbox apps, as well as Win32 apps.

This function should be called during each iteration of the game loop to check when the app enters and exits Game Mode so that the appropriate settings can be applied.

The app must be in the foreground and have focus before exclusive resources are granted.



