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

# PDD_SETEXCLUSIVEMODE callback function


## -description


The <i>DdSetExclusiveMode</i> callback function notifies the driver when a DirectDraw application is switching to or from exclusive mode.


## -parameters




### -param Arg1








#### - lpSetExclusiveMode

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551702">DD_SETEXCLUSIVEMODEDATA</a> structure that contains the notification information.


## -returns



<i>DdSetExclusiveMode</i> returns one of the following callback codes:




## -remarks



<i>DdSetExclusiveMode</i> can be optionally implemented in display drivers. Drivers for hardware that needs to be partially enabled and/or disabled to support exclusive mode should implement this function.

DirectDraw applications can go full screen and take total control of the primary surface. Specifically, the application is responsible for operations such as DirectDraw mode changes and primary surface flipping when in exclusive mode.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551702">DD_SETEXCLUSIVEMODEDATA</a>
 

 

