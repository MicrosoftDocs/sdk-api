---
UID: NC:ddrawint.PDD_CREATEPALETTE
title: PDD_CREATEPALETTE
author: windows-sdk-content
description: The DdCreatePalette callback function creates a DirectDrawPalette object for the specified DirectDraw object.
old-location: display\ddcreatepalette.htm
old-project: display
ms.assetid: 047d63c6-eb4c-4944-8c98-0f9686e2c37a
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: DdCreatePalette, DdCreatePalette callback function [Display Devices], PDD_CREATEPALETTE, PDD_CREATEPALETTE callback, ddfncs_5930e0e6-1029-4c6d-aa6b-b8050e2f9d9d.xml, ddrawint/DdCreatePalette, display.ddcreatepalette
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.redist: 
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
 - DdCreatePalette
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_CREATEPALETTE callback function


## -description


The <b>DdCreatePalette</b> callback function creates a DirectDrawPalette object for the specified DirectDraw object.


## -parameters




### -param Arg1








#### - lpCreatePalette

Points to a <a href="https://msdn.microsoft.com/e43ad510-b44b-4a4d-abb2-10062ce69140">DD_CREATEPALETTEDATA</a> structure that contains the information necessary to create the DirectDrawPalette object.


## -returns



<b>DdCreatePalette</b> returns one of the following callback codes:




## -see-also




<a href="https://msdn.microsoft.com/e43ad510-b44b-4a4d-abb2-10062ce69140">DD_CREATEPALETTEDATA</a>
 

 

