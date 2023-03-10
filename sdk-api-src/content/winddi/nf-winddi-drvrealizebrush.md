---
UID: NF:winddi.DrvRealizeBrush
title: DrvRealizeBrush function (winddi.h)
description: The DrvRealizeBrush function requests that the driver realize a specified brush for a specified surface.
helpviewer_keywords: ["DrvRealizeBrush","DrvRealizeBrush function [Display Devices]","ddifncs_efd25952-e672-493f-80e5-19edbac7df0e.xml","display.drvrealizebrush","winddi/DrvRealizeBrush"]
old-location: display\drvrealizebrush.htm
tech.root: display
ms.assetid: 2948f274-cef2-4fcf-9607-79540b6e5a5f
ms.date: 12/05/2018
ms.keywords: DrvRealizeBrush, DrvRealizeBrush function [Display Devices], ddifncs_efd25952-e672-493f-80e5-19edbac7df0e.xml, display.drvrealizebrush, winddi/DrvRealizeBrush
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvRealizeBrush
 - winddi/DrvRealizeBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvRealizeBrush
---

# DrvRealizeBrush function


## -description

The <b>DrvRealizeBrush</b> function requests that the driver realize a specified brush for a specified surface.

## -parameters

### -param pbo [in]

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that is to be realized. All other parameters, except for <i>psoTarget</i>, can be queried from this object. Parameter specifications are provided as an optimization. This parameter is best used only as a parameter for <a href="/windows/desktop/api/winddi/nf-winddi-brushobj_pvallocrbrush">BRUSHOBJ_pvAllocRbrush</a>, which allocates the memory for the realized brush.

### -param psoTarget [in, out]

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure for which the brush is to be realized. This surface can be the physical surface for the device, a device format bitmap, or a standard format bitmap.

### -param psoPattern [in]

Pointer to the SURFOBJ structure that describes the pattern for the brush. For a raster device, this is a bitmap. For a vector device, this is one of the pattern surfaces provided by <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>.

### -param psoMask [in, optional]

Pointer to a SURFOBJ structure that describes a transparency mask for the brush. This is a 1 bit per pixel bitmap that has the same extent as the pattern. A mask of zero means the pixel is considered a background pixel for the brush. (In transparent background mode, the background pixels are unaffected in a fill.) Plotters can ignore this parameter because they never draw background information.

### -param pxlo [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that defines the interpretation of colors in the pattern. If <i>pxlo</i> is <b>NULL</b>, no translation is needed. A XLATEOBJ_<i>Xxx</i> service routine can be called to translate the colors to device color indices. Vector devices should translate color zero through the XLATEOBJ to get the foreground color for the brush.

### -param iHatch [in]

Specifies whether <i>psoPattern</i> is one of the hatch brushes returned by <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>. This is true if the value of this parameter is less than HS_DDI_MAX, which is defined in <i>winddi.h</i>.

## -returns

The return value is <b>TRUE</b> if the brush was successfully realized. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

To realize a brush, the driver converts a GDI brush into a form that can be used internally. A realized brush contains device-specific information needed by the device to accelerate drawing using the brush.

The driver's realization of a brush is written into the buffer allocated by a call to <a href="/windows/desktop/api/winddi/nf-winddi-brushobj_pvallocrbrush">BRUSHOBJ_pvAllocRbrush</a>.

<b>DrvRealizeBrush</b> is required for a driver that does any drawing to any surface.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-brushobj_pvallocrbrush">BRUSHOBJ_pvAllocRbrush</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>