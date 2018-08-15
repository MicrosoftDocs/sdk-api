---
UID: NC:ddrawint.PDD_FLIPTOGDISURFACE
title: PDD_FLIPTOGDISURFACE
author: windows-sdk-content
description: The DdFlipToGDISurface callback function notifies the driver when DirectDraw is flipping to or from a GDI surface.
old-location: display\ddfliptogdisurface.htm
old-project: display
ms.assetid: 279987bb-1697-4157-9d61-d503b0183e84
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DdFlipToGDISurface, DdFlipToGDISurface callback function [Display Devices], PDD_FLIPTOGDISURFACE, PDD_FLIPTOGDISURFACE callback, ddfncs_667de7ca-b9d4-4267-9d46-79d6c950b51c.xml, ddrawint/DdFlipToGDISurface, display.ddfliptogdisurface
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
 - DdFlipToGDISurface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_FLIPTOGDISURFACE callback function


## -description


The <i>DdFlipToGDISurface</i> callback function notifies the driver when DirectDraw is flipping to or from a GDI surface.


## -parameters




### -param Arg1








#### - lpFlipToGDISurface

Points to a <a href="https://msdn.microsoft.com/ac0fdaf7-0cb2-4474-b3dd-a039161513a4">DD_FLIPTOGDISURFACEDATA</a> structure that contains the notification information.


## -returns



<i>DdFlipToGDISurface</i> returns one of the following callback codes:




## -remarks



<i>DdFlipToGDISurface</i> can be implemented in drivers with hardware that needs to be enabled or disabled, depending on whether a GDI surface is being flipped to.




## -see-also




<a href="https://msdn.microsoft.com/ac0fdaf7-0cb2-4474-b3dd-a039161513a4">DD_FLIPTOGDISURFACEDATA</a>
 

 

