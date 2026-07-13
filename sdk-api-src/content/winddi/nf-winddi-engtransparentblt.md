---
UID: NF:winddi.EngTransparentBlt
title: EngTransparentBlt function (winddi.h)
description: The EngTransparentBlt function provides bit-block transfer capabilities with transparency.
helpviewer_keywords: ["EngTransparentBlt","EngTransparentBlt function [Display Devices]","display.engtransparentblt","gdifncs_1f33c0a3-6062-494c-aef0-2fa368d278ac.xml","winddi/EngTransparentBlt"]
old-location: display\engtransparentblt.htm
tech.root: display
ms.assetid: db98b15f-6b4b-4efc-aa24-20c728b09358
ms.date: 12/05/2018
ms.keywords: EngTransparentBlt, EngTransparentBlt function [Display Devices], display.engtransparentblt, gdifncs_1f33c0a3-6062-494c-aef0-2fa368d278ac.xml, winddi/EngTransparentBlt
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngTransparentBlt
 - winddi/EngTransparentBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-common-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngTransparentBlt
---

# EngTransparentBlt function


## -description

The <b>EngTransparentBlt</b> function provides bit-block transfer capabilities with transparency.

## -parameters

### -param psoDst [in]

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that identifies the target surface on which to draw.

### -param psoSrc [in]

Pointer to the SURFOBJ structure that identifies the source surface of the bit-block transfer.

### -param pco [in, optional]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles. This enumeration limits the area of the destination that is modified. Whenever possible, GDI simplifies the clipping involved.

### -param pxlo [in, optional]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that tells how the source color indices should be translated for writing to the target surface.

### -param prclDst [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines the rectangular area to be modified. This rectangle is specified in the coordinate system of the destination surface and is defined by two points: upper left and lower right. The rectangle is lower-right exclusive; that is, its lower and right edges are not a part of the bit-block transfer. The two points that define the rectangle are always well ordered.

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

The driver should call <b>EngTransparentBlt</b> if it has hooked <a href="/windows/desktop/api/winddi/nf-winddi-drvtransparentblt">DrvTransparentBlt</a> and it is called to do something that it does not support.

Bit-block transfer with transparency is supported between two <a href="/windows-hardware/drivers/">device-managed surfaces</a> or between a device-managed surface and a GDI-managed standard format bitmap. Currently, GDI supports only BMF_4BPP and BMF_8BPP source surfaces.

The pixels on the source surface that match the transparent color specified by <i>iTransparentColor</i> are not copied. For a detailed explanation of transparent blts, see <a href="/windows-hardware/drivers/display/copying-bitmaps">Copying Bitmaps</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvplgblt">DrvPlgBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchbltrop">DrvStretchBltROP</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvtransparentblt">DrvTransparentBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engbitblt">EngBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engplgblt">EngPlgBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engstretchblt">EngStretchBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engstretchbltrop">EngStretchBltROP</a>