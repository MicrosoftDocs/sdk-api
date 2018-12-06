---
UID: NF:winddi.EngTransparentBlt
title: EngTransparentBlt function
author: windows-sdk-content
description: The EngTransparentBlt function provides bit-block transfer capabilities with transparency.
old-location: display\engtransparentblt.htm
tech.root: display
ms.assetid: db98b15f-6b4b-4efc-aa24-20c728b09358
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EngTransparentBlt, EngTransparentBlt function [Display Devices], display.engtransparentblt, gdifncs_1f33c0a3-6062-494c-aef0-2fa368d278ac.xml, winddi/EngTransparentBlt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngTransparentBlt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngTransparentBlt function


## -description


The <b>EngTransparentBlt</b> function provides bit-block transfer capabilities with transparency.


## -parameters




### -param psoDst [in]

Pointer to the <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that identifies the target surface on which to draw.


### -param psoSrc [in]

Pointer to the SURFOBJ structure that identifies the source surface of the bit-block transfer.


### -param pco [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles. This enumeration limits the area of the destination that is modified. Whenever possible, GDI simplifies the clipping involved.


### -param pxlo [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure that tells how the source color indices should be translated for writing to the target surface.


### -param prclDst [in]

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that defines the rectangular area to be modified. This rectangle is specified in the coordinate system of the destination surface and is defined by two points: upper left and lower right. The rectangle is lower-right exclusive; that is, its lower and right edges are not a part of the bit-block transfer. The two points that define the rectangle are always well ordered.

The driver must never call <b>EngTransparentBlt</b> with an empty destination rectangle.


### -param prclSrc [in]

Pointer to a RECTL structure that defines the rectangular area to be copied. This rectangle is specified in the coordinate system of the source surface and is defined by two points: upper left and lower right. The two points that define the rectangle are always well ordered.

The source rectangle will never exceed the bounds of the source surface, and so will never overhang the source surface.

This rectangle is mapped to the destination rectangle defined by <i>prclDst</i>. The driver must never call <b>EngTransparentBlt</b> with an empty source rectangle.


### -param TransColor [in]

Specifies the physical transparent color, in the source surface's format. This is a color index value that has been translated to the source surface's palette. For more information, see the <b>Remarks</b> section.


### -param bCalledFromBitBlt [in]

Reserved. This parameter must be set to zero.


## -returns



<b>EngTransparentBlt</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



The driver should call <b>EngTransparentBlt</b> if it has hooked <a href="https://msdn.microsoft.com/67e61a43-b962-4905-8876-9a0380848ed0">DrvTransparentBlt</a> and it is called to do something that it does not support.

Bit-block transfer with transparency is supported between two <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device-managed surfaces</a> or between a device-managed surface and a GDI-managed standard format bitmap. Currently, GDI supports only BMF_4BPP and BMF_8BPP source surfaces.

The pixels on the source surface that match the transparent color specified by <i>iTransparentColor</i> are not copied. For a detailed explanation of transparent blts, see <a href="https://msdn.microsoft.com/76e07c66-7e57-42d7-b6da-c13c8e9a8dee">Copying Bitmaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/d7b4e25c-b9a1-4200-b449-b7c7ed059db4">DrvBitBlt</a>



<a href="https://msdn.microsoft.com/5bd478f1-0c01-4d7f-9ed1-af84e5bbe773">DrvPlgBlt</a>



<a href="https://msdn.microsoft.com/3520533d-4e42-4abc-bc10-557c674caa33">DrvStretchBlt</a>



<a href="https://msdn.microsoft.com/eeaec7f4-2dfe-42a9-8789-a9ce11aec7b2">DrvStretchBltROP</a>



<a href="https://msdn.microsoft.com/67e61a43-b962-4905-8876-9a0380848ed0">DrvTransparentBlt</a>



<a href="https://msdn.microsoft.com/e99dbe54-485b-4a56-9956-2965f04020db">EngBitBlt</a>



<a href="https://msdn.microsoft.com/a25a0fcd-1a61-483a-ba22-1214a9806b70">EngPlgBlt</a>



<a href="https://msdn.microsoft.com/e8f3084c-6216-497b-923a-adef3bfe8bf7">EngStretchBlt</a>



<a href="https://msdn.microsoft.com/d353fab2-ba5d-42a5-8ce7-04fdc731f6ee">EngStretchBltROP</a>
 

 

