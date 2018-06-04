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

# PDD_SURFCB_ADDATTACHEDSURFACE callback function


## -description


The <b>DdAddAttachedSurface</b> callback function attaches a surface to another surface. 


## -parameters




### -param Arg1








#### - lpAddAttachedSurface

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550462">DD_ADDATTACHEDSURFACEDATA</a> structure that contains information required for the driver to perform the attachment.


## -returns



<b>DdAddAttachedSurface</b> returns one of the following callback codes:




## -remarks



<b>DdAddAttachedSurface</b> can be optionally implemented in DirectDraw drivers.

The driver should update any internal surface state it keeps to reflect the attachment.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550462">DD_ADDATTACHEDSURFACEDATA</a>
 

 

