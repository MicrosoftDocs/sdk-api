---
UID: NC:ddrawint.PDD_VPORTCB_FLIP
title: PDD_VPORTCB_FLIP
author: windows-sdk-content
description: The DdVideoPortFlip callback function performs a physical flip, causing the VPE object to start writing data to the new surface.
old-location: display\ddvideoportflip.htm
old-project: display
ms.assetid: 1e31f33d-84da-40fa-a43c-30ad7d3055e8
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DdVideoPortFlip, DdVideoPortFlip callback function [Display Devices], PDD_VPORTCB_FLIP, PDD_VPORTCB_FLIP callback, ddfncs_a165d7b3-a1c6-4cb6-9087-42d39f6ac96f.xml, ddrawint/DdVideoPortFlip, display.ddvideoportflip
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
 - DdVideoPortFlip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

