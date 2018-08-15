---
UID: NF:winddi.DrvNextBand
title: DrvNextBand function
author: windows-sdk-content
description: The DrvNextBand function is called by GDI when it has finished drawing a band for a physical page, so the driver can send the next band to the printer.
old-location: display\drvnextband.htm
old-project: display
ms.assetid: 7c02d32b-6c95-4dd5-b9cf-2f64ba78f25a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DrvNextBand, DrvNextBand function [Display Devices], ddifncs_dc66e17a-f2da-45cc-bc1a-8058006c6922.xml, display.drvnextband, winddi/DrvNextBand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvNextBand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvNextBand function


## -description


The <b>DrvNextBand</b> function is called by GDI when it has finished drawing a band for a physical page, so the driver can send the next band to the printer.


## -parameters




### -param pso [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure, which identifies the banding surface.


### -param pptl [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure to receive the function-supplied origin of the next band.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.




## -remarks



If a <a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">printer graphics DLL</a> uses GDI-managed surfaces, and if it supports surface banding, it must provide a <b>DrvNextBand</b> function. GDI calls <b>DrvNextBand</b> each time it has finished drawing the portion of the page's image that can be contained on the band's surface. The surface used by GDI for drawing is one that the driver previously specified by calling <a href="https://msdn.microsoft.com/0ee3d697-42aa-4117-9d85-63472e4a042f">EngMarkBandingSurface</a>. The function should send the image to the printer by calling <a href="https://msdn.microsoft.com/c65f09b2-5924-479a-8067-a1ba472348e2">EngWritePrinter</a>, and it should return the indices of the next band's origin in the POINTL structure pointed to by <i>pptl</i>.

After all of a physical page's bands have been drawn, the function should set both members of the POINTL structure pointed to by <i>pptl</i> to -1. 




## -see-also




<a href="https://msdn.microsoft.com/a838a44a-243c-4d0d-bda3-eec9a626cb53">DrvEnableSurface</a>



<a href="https://msdn.microsoft.com/c9006dd1-055b-4fb0-92e8-c7b6bc294941">DrvStartBanding</a>



<a href="https://msdn.microsoft.com/0ee3d697-42aa-4117-9d85-63472e4a042f">EngMarkBandingSurface</a>



<a href="https://msdn.microsoft.com/c65f09b2-5924-479a-8067-a1ba472348e2">EngWritePrinter</a>
 

 

