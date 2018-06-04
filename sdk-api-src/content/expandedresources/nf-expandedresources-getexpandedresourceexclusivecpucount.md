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

# GetExpandedResourceExclusiveCpuCount function


## -description


Gets the expected number of exclusive CPU sets that are available to the app when in Game Mode.


## -parameters




### -param exclusiveCpuCount [out]

The expected number of exclusive CPU sets that are available to the app when in Game Mode.


## -returns



The result of the operation.




## -remarks



This is a Win32 API that's supported in UWP desktop and Xbox apps, as well as Win32 apps.

You can use this function to determine what resources are available to your app, and use this information to decide whether to enter Game Mode or shared mode.

This function returns 0 if no exclusive CPU sets are available, or if the customer opted out of Game Mode via the Settings in Windows 10.

The app must be in the foreground and have focus before exclusive resources are granted.



