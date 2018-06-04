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

# PDD_SURFCB_SETCOLORKEY callback function


## -description


The <i>DdSetColorKey</i> callback function sets the color key value for the specified surface. 


## -parameters




### -param Arg1








#### - lpSetColorKey

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551696">DD_SETCOLORKEYDATA</a> structure that contains the information required to set the color key for the specified surface.


## -returns



<i>DdSetColorKey</i> returns one of the following callback codes:




## -remarks



<i>DdSetColorKey</i> sets the source or destination color key for the specified surface. Typically, this callback is implemented only for drivers that support overlays with color key capabilities.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551696">DD_SETCOLORKEYDATA</a>
 

 

