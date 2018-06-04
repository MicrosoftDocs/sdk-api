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

# PDD_VPORTCB_DESTROYVPORT callback function


## -description


The <b>DdVideoPortDestroy</b> callback function notifies the driver that DirectDraw has destroyed the specified VPE object.


## -parameters




### -param Arg1








#### - lpDestroyVideoPort

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550583">DD_DESTROYVPORTDATA</a> structure that contains the information required for the driver to clean up.


## -returns



<b>DdVideoPortDestroy</b> returns one of the following callback codes:




## -remarks



<b>DdVideoPortDestroy</b> can be optionally implemented in DirectDraw drivers that support VPE.

The driver should free any memory that it allocated and associated with the specified VPE object. This includes freeing any driver-allocated memory accessed through the <b>dwReserved1</b> and <b>dwReserved2</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a> structure. This DD_VIDEOPORT_LOCAL structure is at the <b>lpVideoPort</b> member of the DD_DESTROYVPORTDATA structure at <i>lpDestroyVideoPort</i>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550583">DD_DESTROYVPORTDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a>



<a href="https://msdn.microsoft.com/eeaf3cda-6220-4e8e-8f9e-9f52d1b05ab7">DdVideoPortCreate</a>
 

 

