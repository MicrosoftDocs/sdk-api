---
UID: NC:ddrawint.PDD_VPORTCB_WAITFORSYNC
title: PDD_VPORTCB_WAITFORSYNC
author: windows-sdk-content
description: The DdVideoPortWaitForSync callback function waits until the next vertical synch occurs.
old-location: display\ddvideoportwaitforsync.htm
tech.root: display
ms.assetid: 0834f49b-89c4-47cc-b591-d2b90d21ee72
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DdVideoPortWaitForSync, DdVideoPortWaitForSync callback function [Display Devices], PDD_VPORTCB_WAITFORSYNC, PDD_VPORTCB_WAITFORSYNC callback, ddfncs_11b0544a-9115-4b1f-ab6a-13b870a16ecc.xml, ddrawint/DdVideoPortWaitForSync, display.ddvideoportwaitforsync
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
 - DdVideoPortWaitForSync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_VPORTCB_WAITFORSYNC callback function


## -description


The <i>DdVideoPortWaitForSync</i> callback function waits until the next vertical synch occurs.


## -parameters




### -param Arg1








#### - lpWaitForSync

Points to a <a href="https://msdn.microsoft.com/903c697e-4fa5-472e-ab5b-7864a326f323">DD_WAITFORVPORTSYNCDATA</a> structure that contains the information required for the driver to synchronize the VPE object.


## -returns



<i>DdVideoPortWaitForSync</i> returns one of the following callback codes:




## -remarks



If the condition on which the driver is waiting does not occur before the number of milliseconds specified in the  <b>dwTimeOut</b> member of the DD_WAITFORVPORTSYNCDATA structure at <i>lpWaitForSync</i> has elapsed, the driver should set the <b>ddRVal</b> member of <a href="https://msdn.microsoft.com/903c697e-4fa5-472e-ab5b-7864a326f323">DD_WAITFORVPORTSYNCDATA</a> to DDERR_VIDEONOTACTIVE and return DDHAL_DRIVER_HANDLED.

The driver must specify its own time-out criteria when <b>dwTimeOut</b> is zero.




## -see-also




<a href="https://msdn.microsoft.com/903c697e-4fa5-472e-ab5b-7864a326f323">DD_WAITFORVPORTSYNCDATA</a>
 

 

