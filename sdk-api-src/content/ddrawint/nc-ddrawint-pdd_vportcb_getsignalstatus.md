---
UID: NC:ddrawint.PDD_VPORTCB_GETSIGNALSTATUS
title: PDD_VPORTCB_GETSIGNALSTATUS
author: windows-sdk-content
description: The DdVideoPortGetSignalStatus callback function retrieves the status of the video signal currently being presented to the hardware video port.
old-location: display\ddvideoportgetsignalstatus.htm
old-project: display
ms.assetid: d3868acf-b119-4ab3-aa85-64d50f76fdb7
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: DdVideoPortGetSignalStatus, DdVideoPortGetSignalStatus callback function [Display Devices], PDD_VPORTCB_GETSIGNALSTATUS, PDD_VPORTCB_GETSIGNALSTATUS callback, ddfncs_ed14dce3-e341-436b-90b4-1175b2eae121.xml, ddrawint/DdVideoPortGetSignalStatus, display.ddvideoportgetsignalstatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdVideoPortGetSignalStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_VPORTCB_GETSIGNALSTATUS callback function


## -description


The <i>DdVideoPortGetSignalStatus</i> callback function retrieves the status of the video signal currently being presented to the hardware video port.


## -parameters




### -param Arg1








#### - lpGetSignalStatus

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551620">DD_GETVPORTSIGNALDATA</a> structure that contains the information required for the driver to retrieve the status of the video signal.


## -returns



<i>DdVideoPortGetSignalStatus</i> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support VPE must implement <i>DdVideoPortGetSignalStatus</i>.

The driver should determine whether a valid signal is coming in to the hardware video port and report the result in the <b>dwStatus</b> member of the DD_GETVPORTSIGNALDATA structure at <i>lpGetSignalStatus</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551620">DD_GETVPORTSIGNALDATA</a>
 

 

