---
UID: NF:winddi.DrvCopyBits
title: DrvCopyBits function
author: windows-sdk-content
description: The DrvCopyBits function translates between device-managed raster surfaces and GDI standard-format bitmaps.
old-location: display\drvcopybits.htm
old-project: display
ms.assetid: c2d42c7a-3d6e-416c-a194-2228cc1b0fd9
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: DrvCopyBits, DrvCopyBits function [Display Devices], ddifncs_95bc17c2-b4ae-4883-8866-cd9dded1f30d.xml, display.drvcopybits, winddi/DrvCopyBits
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	DrvCopyBits
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvCopyBits function


## -description


The <b>DrvCopyBits</b> function translates between device-managed raster surfaces and GDI standard-format bitmaps. 


## -parameters




### -param psoDest

Pointer to the destination <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure for the copy operation.


### -param psoSrc

Pointer to the source SURFOBJ structure for the copy operation.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure that defines a clip region on the destination surface.


### -param pxlo

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a> structure that defines the translation of color indices between the source and target surfaces. If <i>pxlo</i> is <b>NULL</b>, no translation is needed.


### -param prclDest

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that defines the area to be modified. This structure uses the coordinate system of the destination surface. The lower and right edges of this rectangle are not part of the bit-block transfer, meaning the rectangle is lower right exclusive.

<b>DrvCopyBits</b> is never called with an empty destination rectangle. The two points that define the rectangle are always well-ordered.


### -param pptlSrc

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that defines the upper-left corner of the source rectangle.


## -returns



The return value is <b>TRUE</b> if the source surface is successfully copied to the destination surface.




## -remarks



The driver may optionally hook <b>DrvCopyBits</b>. If so, GDI will call <b>DrvCopyBits</b> when it needs to copy from one surface to another and at least one of the surfaces is device-managed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a>
 

 

