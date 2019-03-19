---
UID: NC:ddrawint.PDD_COLORCB_COLORCONTROL
title: PDD_COLORCB_COLORCONTROL (ddrawint.h)
author: windows-sdk-content
description: The DdControlColor callback function controls the luminance and brightness controls of an overlay surface.
old-location: display\ddcontrolcolor.htm
tech.root: display
ms.assetid: 626fdd37-bebb-47b7-9899-7cf0dc2bd1ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DdControlColor, DdControlColor callback function [Display Devices], PDD_COLORCB_COLORCONTROL, PDD_COLORCB_COLORCONTROL callback, ddfncs_c79505e9-282b-469f-ae35-19a9644aecae.xml, ddrawint/DdControlColor, display.ddcontrolcolor
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
 - DdControlColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_COLORCB_COLORCONTROL callback function


## -description


The <b>DdControlColor</b> callback function controls the luminance and brightness controls of an overlay surface.  


## -parameters




### -param Arg1








#### - lpColorControl

Points to a <a href="https://msdn.microsoft.com/7c983faa-de9d-4a04-ac8d-d37fb182a662">DD_COLORCONTROLDATA</a> structure that contains the color control information for a specified overlay surface.


## -returns



<b>DdControlColor</b> returns one of the following callback codes:




## -remarks



<b>DdControlColor</b> can be optionally implemented in a DirectDraw driver.




## -see-also




<a href="https://msdn.microsoft.com/7c983faa-de9d-4a04-ac8d-d37fb182a662">DD_COLORCONTROLDATA</a>
 

 

