---
UID: NC:ddrawint.PDD_SURFCB_SETPALETTE
title: PDD_SURFCB_SETPALETTE
author: windows-sdk-content
description: The DdSetPalette callback function attaches a palette to the specified surface.
old-location: display\ddsetpalette.htm
tech.root: display
ms.assetid: 745b30f0-3d2f-4894-8991-6b7d511f8493
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DdSetPalette, DdSetPalette callback function [Display Devices], PDD_SURFCB_SETPALETTE, PDD_SURFCB_SETPALETTE callback, ddfncs_7d4146b2-d5f8-4a02-b24e-3dfa0a8d817a.xml, ddrawint/DdSetPalette, display.ddsetpalette
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
 - DdSetPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_SURFCB_SETPALETTE callback function


## -description


The <b>DdSetPalette</b> callback function attaches a palette to the specified surface.


## -parameters




### -param Arg1








#### - lpSetPalette

Points to a <a href="https://msdn.microsoft.com/943af430-19b2-481a-9cac-cd4cb767d96a">DD_SETPALETTEDATA</a> structure that contains the information required to set a palette to the specified surface.


## -returns



<b>DdSetPalette</b> returns one of the following callback codes:




## -see-also




<a href="https://msdn.microsoft.com/943af430-19b2-481a-9cac-cd4cb767d96a">DD_SETPALETTEDATA</a>
 

 

