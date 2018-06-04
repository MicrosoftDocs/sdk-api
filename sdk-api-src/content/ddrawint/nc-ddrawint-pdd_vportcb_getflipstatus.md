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

# PDD_VPORTCB_GETFLIPSTATUS callback function


## -description


The <i>DdVideoPortGetFlipStatus</i> callback function determines whether the most recently requested flip on a surface has occurred.


## -parameters




### -param Arg1








#### - lpGetFlipStatus

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551604">DD_GETVPORTFLIPSTATUSDATA</a> structure that contains the information required for the driver to determine a surface's flip status.


## -returns



<i>DdVideoPortGetFlipStatus</i> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support VPE must implement <i>DdVideoPortGetFlipStatus</i>.

The driver should set the <b>ddRVal</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551604">DD_GETVPORTFLIPSTATUSDATA</a> structure at <i>lpGetFlipStatus</i> to DDERR_WASSTILLDRAWING and return DDHAL_DRIVER_HANDLED if a flip is currently in progress; otherwise the driver should set <b>ddRVal</b> to DD_OK and return DDHAL_DRIVER_HANDLED.

If the driver sets <b>ddRVal</b> to DDERR_WASSTILLDRAWING, DirectDraw will fail locks and blits on that surface.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551604">DD_GETVPORTFLIPSTATUSDATA</a>
 

 

