---
UID: NC:ddrawint.PDD_PALCB_DESTROYPALETTE
title: PDD_PALCB_DESTROYPALETTE
author: windows-driver-content
description: The DdDestroyPalette callback function destroys the specified palette.
old-location: display\dddestroypalette.htm
old-project: display
ms.assetid: b44936fd-0052-4f54-9e97-1664c381c697
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DdDestroyPalette, DdDestroyPalette callback function [Display Devices], PDD_PALCB_DESTROYPALETTE, PDD_PALCB_DESTROYPALETTE callback, ddfncs_a0c991ff-d3b8-4793-a6b3-a72dc5f5d700.xml, ddrawint/DdDestroyPalette, display.dddestroypalette
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
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ddrawint.h
api_name:
-	DdDestroyPalette
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_PALCB_DESTROYPALETTE callback function


## -description


The <b>DdDestroyPalette</b> callback function destroys the specified palette.


## -parameters




### -param Arg1








#### - lpDestroyPalette

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550574">DD_DESTROYPALETTEDATA</a> structure that contains the information needed to destroy a palette.


## -returns



<b>DdDestroyPalette</b> returns one of the following callback codes:




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550574">DD_DESTROYPALETTEDATA</a>
 

 

