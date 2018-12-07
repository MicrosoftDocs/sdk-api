---
UID: NC:ddrawint.PDD_VPORTCB_GETFLIPSTATUS
title: PDD_VPORTCB_GETFLIPSTATUS
author: windows-sdk-content
description: The DdVideoPortGetFlipStatus callback function determines whether the most recently requested flip on a surface has occurred.
old-location: display\ddvideoportgetflipstatus.htm
tech.root: display
ms.assetid: 67a7aa80-2201-4bb7-919b-dd9ca1228f06
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DdVideoPortGetFlipStatus, DdVideoPortGetFlipStatus callback function [Display Devices], PDD_VPORTCB_GETFLIPSTATUS, PDD_VPORTCB_GETFLIPSTATUS callback, ddfncs_b5004bc9-0486-40b0-9be0-b17b10b0241a.xml, ddrawint/DdVideoPortGetFlipStatus, display.ddvideoportgetflipstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdVideoPortGetFlipStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_VPORTCB_GETFLIPSTATUS callback function


## -description


The <i>DdVideoPortGetFlipStatus</i> callback function determines whether the most recently requested flip on a surface has occurred.


## -parameters




### -param Arg1








#### - lpGetFlipStatus

Points to a <a href="https://msdn.microsoft.com/64be9019-a75f-42db-a636-b767f87c1858">DD_GETVPORTFLIPSTATUSDATA</a> structure that contains the information required for the driver to determine a surface's flip status.


## -returns



<i>DdVideoPortGetFlipStatus</i> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support VPE must implement <i>DdVideoPortGetFlipStatus</i>.

The driver should set the <b>ddRVal</b> member of the <a href="https://msdn.microsoft.com/64be9019-a75f-42db-a636-b767f87c1858">DD_GETVPORTFLIPSTATUSDATA</a> structure at <i>lpGetFlipStatus</i> to DDERR_WASSTILLDRAWING and return DDHAL_DRIVER_HANDLED if a flip is currently in progress; otherwise the driver should set <b>ddRVal</b> to DD_OK and return DDHAL_DRIVER_HANDLED.

If the driver sets <b>ddRVal</b> to DDERR_WASSTILLDRAWING, DirectDraw will fail locks and blits on that surface.




## -see-also




<a href="https://msdn.microsoft.com/64be9019-a75f-42db-a636-b767f87c1858">DD_GETVPORTFLIPSTATUSDATA</a>
 

 

