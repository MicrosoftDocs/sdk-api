---
UID: NF:winddi.DrvCopyBits
title: DrvCopyBits function
author: windows-sdk-content
description: The DrvCopyBits function translates between device-managed raster surfaces and GDI standard-format bitmaps.
old-location: display\drvcopybits.htm
tech.root: display
ms.assetid: c2d42c7a-3d6e-416c-a194-2228cc1b0fd9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DrvCopyBits, DrvCopyBits function [Display Devices], ddifncs_95bc17c2-b4ae-4883-8866-cd9dded1f30d.xml, display.drvcopybits, winddi/DrvCopyBits
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
 - DrvCopyBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DrvCopyBits
: 
---

# DrvCopyBits function


## -description


The <b>DrvCopyBits</b> function translates between device-managed raster surfaces and GDI standard-format bitmaps. 


## -parameters




### -param psoDest

Pointer to the destination <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure for the copy operation.


### -param psoSrc

Pointer to the source SURFOBJ structure for the copy operation.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure that defines a clip region on the destination surface.


### -param pxlo

Pointer to an <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure that defines the translation of color indices between the source and target surfaces. If <i>pxlo</i> is <b>NULL</b>, no translation is needed.


### -param prclDest

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that defines the area to be modified. This structure uses the coordinate system of the destination surface. The lower and right edges of this rectangle are not part of the bit-block transfer, meaning the rectangle is lower right exclusive.

<b>DrvCopyBits</b> is never called with an empty destination rectangle. The two points that define the rectangle are always well-ordered.


### -param pptlSrc

Pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that defines the upper-left corner of the source rectangle.


## -returns



The return value is <b>TRUE</b> if the source surface is successfully copied to the destination surface.




## -remarks



The driver may optionally hook <b>DrvCopyBits</b>. If so, GDI will call <b>DrvCopyBits</b> when it needs to copy from one surface to another and at least one of the surfaces is device-managed.




## -see-also




<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a>
 

 

