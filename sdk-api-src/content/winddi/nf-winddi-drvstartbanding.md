---
UID: NF:winddi.DrvStartBanding
title: DrvStartBanding function
author: windows-sdk-content
description: The DrvStartBanding function is called by GDI when it is ready to start sending bands of a physical page to the driver for rendering.
old-location: display\drvstartbanding.htm
tech.root: display
ms.assetid: c9006dd1-055b-4fb0-92e8-c7b6bc294941
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: DrvStartBanding, DrvStartBanding function [Display Devices], ddifncs_d0cd5c63-cf46-472a-be6c-8d9dd124a2b2.xml, display.drvstartbanding, winddi/DrvStartBanding
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
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
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvStartBanding
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvStartBanding function


## -description


The <b>DrvStartBanding</b> function is called by GDI when it is ready to start sending bands of a physical page to the driver for rendering.


## -parameters




### -param pso [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure, which identifies the banding surface.


### -param pptl [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure to receive the function-supplied origin of the first band.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.




## -remarks



If a printer graphics DLL uses GDI-managed surfaces, and if it supports surface banding, it must provide a <a href="https://msdn.microsoft.com/7c02d32b-6c95-4dd5-b9cf-2f64ba78f25a">DrvNextBand</a> function. GDI calls <b>DrvStartBanding</b> only if the printer graphics DLL's <a href="https://msdn.microsoft.com/a838a44a-243c-4d0d-bda3-eec9a626cb53">DrvEnableSurface</a> function previously called <a href="https://msdn.microsoft.com/0ee3d697-42aa-4117-9d85-63472e4a042f">EngMarkBandingSurface</a> to specify a banding surface.

The <b>DrvStartBanding</b> function's purpose is to allow the printer graphics DLL to perform any initializations needed before banding operations begin on a physical page, and to provide GDI with the indices of the first band's origin.

The <b>DrvStartBanding</b> function is called once per page. Each time GDI has finished drawing a band, it calls <a href="https://msdn.microsoft.com/7c02d32b-6c95-4dd5-b9cf-2f64ba78f25a">DrvNextBand</a> so the driver can send the band to the printer.




## -see-also




<a href="https://msdn.microsoft.com/a838a44a-243c-4d0d-bda3-eec9a626cb53">DrvEnableSurface</a>



<a href="https://msdn.microsoft.com/7c02d32b-6c95-4dd5-b9cf-2f64ba78f25a">DrvNextBand</a>



<a href="https://msdn.microsoft.com/0ee3d697-42aa-4117-9d85-63472e4a042f">EngMarkBandingSurface</a>
 

 

