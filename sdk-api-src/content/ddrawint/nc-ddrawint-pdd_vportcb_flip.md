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

# PDD_VPORTCB_FLIP callback function


## -description


The <i>DdVideoPortFlip</i> callback function performs a physical flip, causing the VPE object to start writing data to the new surface.


## -parameters




### -param Arg1








#### - lpFlipVideoPort

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551523">DD_FLIPVPORTDATA</a> structure that contains the information required for the driver to perform the flip.


## -returns



<i>DdVideoPortFlip</i> returns one of the following callback codes:




## -remarks



<i>DdVideoPortFlip</i> must be implemented in DirectDraw drivers that support VPE.

The driver should update its surface pointers so that the next frame of video will be written to the surface to which the <b>lpSurfTarg</b> member of the DD_FLIPVPORTDATA structure at <i>lpFlipVideoPort</i> points. If a previous flip request is still pending, the driver should fail the call by setting the <b>ddRVal</b> member of DD_FLIPVPORTDATA to DDERR_WASSTILLDRAWING and returning DDHAL_DRIVER_HANDLED. <i>DdVideoPortFlip</i> does not affect the actual display of the video data.

A call to <i>DdVideoPortFlip</i> typically accompanies a call to <a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a> when an application is performing video streaming.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551523">DD_FLIPVPORTDATA</a>



<a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a>
 

 

