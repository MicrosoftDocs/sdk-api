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
 

 

