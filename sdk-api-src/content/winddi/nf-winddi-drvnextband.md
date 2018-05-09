---
UID: NF:winddi.DrvNextBand
title: DrvNextBand function
author: windows-driver-content
description: The DrvNextBand function is called by GDI when it has finished drawing a band for a physical page, so the driver can send the next band to the printer.
old-location: display\drvnextband.htm
old-project: display
ms.assetid: 7c02d32b-6c95-4dd5-b9cf-2f64ba78f25a
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DrvNextBand, DrvNextBand function [Display Devices], ddifncs_dc66e17a-f2da-45cc-bc1a-8058006c6922.xml, display.drvnextband, winddi/DrvNextBand
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	DrvNextBand
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

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure, which identifies the banding surface.


### -param pptl [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure to receive the function-supplied origin of the next band.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.




## -remarks



If a <a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">printer graphics DLL</a> uses GDI-managed surfaces, and if it supports surface banding, it must provide a <b>DrvNextBand</b> function. GDI calls <b>DrvNextBand</b> each time it has finished drawing the portion of the page's image that can be contained on the band's surface. The surface used by GDI for drawing is one that the driver previously specified by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564975">EngMarkBandingSurface</a>. The function should send the image to the printer by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a>, and it should return the indices of the next band's origin in the POINTL structure pointed to by <i>pptl</i>.

After all of a physical page's bands have been drawn, the function should set both members of the POINTL structure pointed to by <i>pptl</i> to -1. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556292">DrvStartBanding</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564975">EngMarkBandingSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a>
 

 

