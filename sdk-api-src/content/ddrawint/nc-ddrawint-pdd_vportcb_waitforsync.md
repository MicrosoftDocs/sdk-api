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

# PDD_VPORTCB_WAITFORSYNC callback function


## -description


The <i>DdVideoPortWaitForSync</i> callback function waits until the next vertical synch occurs.


## -parameters




### -param Arg1








#### - lpWaitForSync

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551772">DD_WAITFORVPORTSYNCDATA</a> structure that contains the information required for the driver to synchronize the VPE object.


## -returns



<i>DdVideoPortWaitForSync</i> returns one of the following callback codes:




## -remarks



If the condition on which the driver is waiting does not occur before the number of milliseconds specified in the  <b>dwTimeOut</b> member of the DD_WAITFORVPORTSYNCDATA structure at <i>lpWaitForSync</i> has elapsed, the driver should set the <b>ddRVal</b> member of <a href="https://msdn.microsoft.com/library/windows/hardware/ff551772">DD_WAITFORVPORTSYNCDATA</a> to DDERR_VIDEONOTACTIVE and return DDHAL_DRIVER_HANDLED.

The driver must specify its own time-out criteria when <b>dwTimeOut</b> is zero.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551772">DD_WAITFORVPORTSYNCDATA</a>
 

 

