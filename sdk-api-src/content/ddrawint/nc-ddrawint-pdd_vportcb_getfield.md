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

# PDD_VPORTCB_GETFIELD callback function


## -description


The <b>DdVideoPortGetField</b> callback function determines whether the current field of an interlaced signal is even or odd.


## -parameters




### -param Arg1








#### - lpGetField

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551598">DD_GETVPORTFIELDDATA</a> structure that contains the information required for the driver to determine whether the current field is even or odd.


## -returns



<b>DdVideoPortGetField</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that set the DDVPCAPS_READBACKFIELD flag in the <b>dwCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550376">DDVIDEOPORTCAPS</a> structure must implement <b>DdVideoPortGetField</b>.

The driver should determine whether the current field is even or odd and write <b>TRUE</b> or <b>FALSE</b> in the <b>bField</b> member of the DD_GETVPORTFIELDDATA structure at <b>lpGetField</b>, accordingly. If the query cannot be performed because the hardware video port is disabled, the driver should return DDHAL_DRIVER_HANDLED and set DDERR_VIDEONOTACTIVE in the <b>ddRVal</b> member of DD_GETVPORTFIELDDATA.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550376">DDVIDEOPORTCAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551598">DD_GETVPORTFIELDDATA</a>
 

 

