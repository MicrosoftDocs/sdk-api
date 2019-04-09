---
UID: NC:ddrawint.PDD_SETEXCLUSIVEMODE
title: PDD_SETEXCLUSIVEMODE (ddrawint.h)
author: windows-sdk-content
description: The DdSetExclusiveMode callback function notifies the driver when a DirectDraw application is switching to or from exclusive mode.
old-location: display\ddsetexclusivemode.htm
tech.root: display
ms.assetid: c322a4ac-0900-4f31-9e02-923afdad5fd6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DdSetExclusiveMode, DdSetExclusiveMode callback function [Display Devices], PDD_SETEXCLUSIVEMODE, PDD_SETEXCLUSIVEMODE callback, ddfncs_5ac6ee85-d0b5-414d-89c6-01f8a1e11488.xml, ddrawint/DdSetExclusiveMode, display.ddsetexclusivemode
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
 - DdSetExclusiveMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_SETEXCLUSIVEMODE callback function


## -description


The <i>DdSetExclusiveMode</i> callback function notifies the driver when a DirectDraw application is switching to or from exclusive mode.


## -parameters




### -param Arg1








#### - lpSetExclusiveMode

Points to a <a href="https://msdn.microsoft.com/b2f5af15-c773-4741-a8dc-71d2b89776a7">DD_SETEXCLUSIVEMODEDATA</a> structure that contains the notification information.


## -returns



<i>DdSetExclusiveMode</i> returns one of the following callback codes:




## -remarks



<i>DdSetExclusiveMode</i> can be optionally implemented in display drivers. Drivers for hardware that needs to be partially enabled and/or disabled to support exclusive mode should implement this function.

DirectDraw applications can go full screen and take total control of the primary surface. Specifically, the application is responsible for operations such as DirectDraw mode changes and primary surface flipping when in exclusive mode.




## -see-also




<a href="https://msdn.microsoft.com/b2f5af15-c773-4741-a8dc-71d2b89776a7">DD_SETEXCLUSIVEMODEDATA</a>
 

 

