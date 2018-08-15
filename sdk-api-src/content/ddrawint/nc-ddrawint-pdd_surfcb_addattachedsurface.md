---
UID: NC:ddrawint.PDD_SURFCB_ADDATTACHEDSURFACE
title: PDD_SURFCB_ADDATTACHEDSURFACE
author: windows-sdk-content
description: The DdAddAttachedSurface callback function attaches a surface to another surface.
old-location: display\ddaddattachedsurface.htm
old-project: display
ms.assetid: 53f146e6-f521-4c95-b98b-0e8acb994c9d
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DdAddAttachedSurface, DdAddAttachedSurface callback function [Display Devices], PDD_SURFCB_ADDATTACHEDSURFACE, PDD_SURFCB_ADDATTACHEDSURFACE callback, ddfncs_b7f5d56d-95b7-4b79-8d20-9ab663582dd2.xml, ddrawint/DdAddAttachedSurface, display.ddaddattachedsurface
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
 - DdAddAttachedSurface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_SURFCB_ADDATTACHEDSURFACE callback function


## -description


The <b>DdAddAttachedSurface</b> callback function attaches a surface to another surface. 


## -parameters




### -param Arg1








#### - lpAddAttachedSurface

Points to a <a href="https://msdn.microsoft.com/d00120d9-5825-4998-a1ef-ccc5654b91b9">DD_ADDATTACHEDSURFACEDATA</a> structure that contains information required for the driver to perform the attachment.


## -returns



<b>DdAddAttachedSurface</b> returns one of the following callback codes:




## -remarks



<b>DdAddAttachedSurface</b> can be optionally implemented in DirectDraw drivers.

The driver should update any internal surface state it keeps to reflect the attachment.




## -see-also




<a href="https://msdn.microsoft.com/d00120d9-5825-4998-a1ef-ccc5654b91b9">DD_ADDATTACHEDSURFACEDATA</a>
 

 

