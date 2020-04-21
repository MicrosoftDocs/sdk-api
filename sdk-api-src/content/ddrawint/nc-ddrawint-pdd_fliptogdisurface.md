---
UID: NC:ddrawint.PDD_FLIPTOGDISURFACE
title: PDD_FLIPTOGDISURFACE (ddrawint.h)
description: The DdFlipToGDISurface callback function notifies the driver when DirectDraw is flipping to or from a GDI surface.helpviewer_keywords: ["DdFlipToGDISurface","DdFlipToGDISurface callback function [Display Devices]","PDD_FLIPTOGDISURFACE","PDD_FLIPTOGDISURFACE callback","ddfncs_667de7ca-b9d4-4267-9d46-79d6c950b51c.xml","ddrawint/DdFlipToGDISurface","display.ddfliptogdisurface"]
old-location: display\ddfliptogdisurface.htm
tech.root: display
ms.assetid: 279987bb-1697-4157-9d61-d503b0183e84
ms.date: 12/05/2018
ms.keywords: DdFlipToGDISurface, DdFlipToGDISurface callback function [Display Devices], PDD_FLIPTOGDISURFACE, PDD_FLIPTOGDISURFACE callback, ddfncs_667de7ca-b9d4-4267-9d46-79d6c950b51c.xml, ddrawint/DdFlipToGDISurface, display.ddfliptogdisurface
f1_keywords:
- ddrawint/DdFlipToGDISurface
dev_langs:
- c++
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
- DdFlipToGDISurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDD_FLIPTOGDISURFACE callback function


## -description


The <i>DdFlipToGDISurface</i> callback function notifies the driver when DirectDraw is flipping to or from a GDI surface.


## -parameters




### -param Arg1








#### - lpFlipToGDISurface

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_fliptogdisurfacedata">DD_FLIPTOGDISURFACEDATA</a> structure that contains the notification information.


## -returns



<i>DdFlipToGDISurface</i> returns one of the following callback codes:




## -remarks



<i>DdFlipToGDISurface</i> can be implemented in drivers with hardware that needs to be enabled or disabled, depending on whether a GDI surface is being flipped to.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_fliptogdisurfacedata">DD_FLIPTOGDISURFACEDATA</a>
 

 

