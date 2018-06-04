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

# PDD_FLIPTOGDISURFACE callback function


## -description


The <i>DdFlipToGDISurface</i> callback function notifies the driver when DirectDraw is flipping to or from a GDI surface.


## -parameters




### -param Arg1








#### - lpFlipToGDISurface

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551522">DD_FLIPTOGDISURFACEDATA</a> structure that contains the notification information.


## -returns



<i>DdFlipToGDISurface</i> returns one of the following callback codes:




## -remarks



<i>DdFlipToGDISurface</i> can be implemented in drivers with hardware that needs to be enabled or disabled, depending on whether a GDI surface is being flipped to.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551522">DD_FLIPTOGDISURFACEDATA</a>
 

 

