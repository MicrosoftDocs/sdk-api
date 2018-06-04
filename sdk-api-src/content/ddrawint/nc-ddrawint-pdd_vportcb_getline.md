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

# PDD_VPORTCB_GETLINE callback function


## -description


The <b>DdVideoPortGetLine</b> callback function returns the current line number of the hardware video port.


## -parameters




### -param Arg1








#### - lpGetLine

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551610">DD_GETVPORTLINEDATA</a> structure that contains the information required for the driver to determine and return the current line number for the specified hardware video port.


## -returns



<b>DdVideoPortGetLine</b> returns one of the following callback codes:




## -remarks



Drivers that set the DDVPCAPS_READBACKLINE flag in the <b>dwCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550376">DDVIDEOPORTCAPS</a> structure must implement <b>DdVideoPortGetLine</b>.

The driver should write the number of the current video line in the <b>dwLine</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551610">DD_GETVPORTLINEDATA</a> structure at <i>lpGetLine</i>. The returned line number must be zero-based; that is, the first line of video is line 0, the second line of video is line 1, etc.

If the device is in a vertical blank, the driver should set DDERR_VERTICALBLANKINPROGRESS in the <b>ddRVal</b> member of <a href="https://msdn.microsoft.com/library/windows/hardware/ff551610">DD_GETVPORTLINEDATA</a>. If the query cannot be performed because the hardware video port is disabled, the driver should set DDERR_VIDEONOTACTIVE in <b>ddRVal</b>. In both of these failed cases, the driver should return DDHAL_DRIVER_HANDLED.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550376">DDVIDEOPORTCAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551610">DD_GETVPORTLINEDATA</a>
 

 

