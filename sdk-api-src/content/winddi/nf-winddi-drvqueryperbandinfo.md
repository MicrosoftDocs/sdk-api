---
UID: NF:winddi.DrvQueryPerBandInfo
title: DrvQueryPerBandInfo function (winddi.h)
description: A printer graphics DLL's DrvQueryPerBandInfo function is called by GDI before it begins drawing a band for a physical page, so the driver can supply GDI with band-specific information.
helpviewer_keywords: ["DrvQueryPerBandInfo","DrvQueryPerBandInfo function [Display Devices]","ddifncs_8a5e262c-23e5-4e49-bd36-6674efe7090f.xml","display.drvqueryperbandinfo","winddi/DrvQueryPerBandInfo"]
old-location: display\drvqueryperbandinfo.htm
tech.root: display
ms.assetid: 2e2c1aa7-9ba4-4bf9-acfb-43212d3d4899
ms.date: 12/05/2018
ms.keywords: DrvQueryPerBandInfo, DrvQueryPerBandInfo function [Display Devices], ddifncs_8a5e262c-23e5-4e49-bd36-6674efe7090f.xml, display.drvqueryperbandinfo, winddi/DrvQueryPerBandInfo
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
 - DrvQueryPerBandInfo
 - winddi/DrvQueryPerBandInfo
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
 - DrvQueryPerBandInfo
---

# DrvQueryPerBandInfo function


## -description

A printer graphics DLL's <b>DrvQueryPerBandInfo</b> function is called by GDI before it begins drawing a band for a physical page, so the driver can supply GDI with band-specific information.

## -parameters

### -param pso [in]

Caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure describing the drawing surface.

### -param pbi [in, out]

Caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-perbandinfo">PERBANDINFO</a> structure containing default information, which the function can overwrite.

## -returns

The function must return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Greater than zero</b></dt>
</dl>
</td>
<td width="60%">
GDI will use the contents of the PERBANDINFO structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
GDI will ignore the contents of the PERBANDINFO structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDI_ERROR</b></dt>
</dl>
</td>
<td width="60%">
GDI will not draw the band.

</td>
</tr>
</table>

## -remarks

If a <a href="/windows-hardware/drivers/print/printer-graphics-dll">printer graphics DLL</a> uses GDI-managed surfaces, and if it supports surface banding, it can optionally provide a <b>DrvQueryPerBandInfo</b> function. GDI calls the function prior to rendering each band.

The printer graphics DLL uses the function's <a href="/windows/desktop/api/winddi/ns-winddi-perbandinfo">PERBANDINFO</a> structure to indicate whether the previous band should be redrawn, and to specify that the band should be scaled. If a printer graphics DLL supports banding but does not provide a <b>DrvQueryPerBandInfo</b> function, GDI will not repeat or scale bands.

The <b>DrvQueryPerBandInfo</b> function is only called during playback of EMF files.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvnextband">DrvNextBand</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstartbanding">DrvStartBanding</a>