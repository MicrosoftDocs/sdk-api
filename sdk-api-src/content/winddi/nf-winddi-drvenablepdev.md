---
UID: NF:winddi.DrvEnablePDEV
title: DrvEnablePDEV function (winddi.h)
description: The DrvEnablePDEV function returns a description of the physical device's characteristics to GDI.
helpviewer_keywords: ["DrvEnablePDEV","DrvEnablePDEV function [Display Devices]","ddifncs_62a5b81b-a608-4da0-8315-3268fb6f65da.xml","display.drvenablepdev","winddi/DrvEnablePDEV"]
old-location: display\drvenablepdev.htm
tech.root: display
ms.assetid: 9a7ed18a-f21c-486b-9261-59a3fe5aef9e
ms.date: 12/05/2018
ms.keywords: DrvEnablePDEV, DrvEnablePDEV function [Display Devices], ddifncs_62a5b81b-a608-4da0-8315-3268fb6f65da.xml, display.drvenablepdev, winddi/DrvEnablePDEV
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
 - DrvEnablePDEV
 - winddi/DrvEnablePDEV
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
 - DrvEnablePDEV
---

# DrvEnablePDEV function


## -description

The <b>DrvEnablePDEV</b> function returns a description of the physical device's characteristics to GDI.

## -parameters

### -param pdm [in]

Pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODEW</a> structure that contains driver data. 

For a driver that supports Windows NT 4.0, <b>DrvEnablePDEV</b> should return the default mode of the hardware when GDI calls it with the following <a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODEW</a> members set to zero: <b>dmBitsPerPel</b>, <b>dmPelsWidth</b>, <b>dmPelsHeight</b>, and <b>dmDisplayFrequency</b>.

### -param pwszLogAddress [in]

For printer drivers, points to the logical address string that is the user's name for the location to which the driver is writing. Examples include "LPT1" or "My Printer."

Display drivers should ignore this parameter.

### -param cPat

For printer drivers, specifies the number of surface handles in the buffer pointed to by <i>phsurfPatterns</i>. The driver cannot access memory beyond the end of the buffer.

Display drivers should ignore this parameter.

### -param phsurfPatterns [in, optional]

Display drivers should ignore this parameter.

For printer drivers, points to a buffer that the driver will fill with surface handles representing the standard fill patterns. The following patterns must be defined in order:

<table>
<tr>
<th>Pattern</th>
<th>Description</th>
</tr>
<tr>
<td>
HS_HORIZONTAL

</td>
<td>
Horizontal hatch.

</td>
</tr>
<tr>
<td>
HS_VERTICAL

</td>
<td>
Vertical hatch.

</td>
</tr>
<tr>
<td>
HS_FDIAGONAL

</td>
<td>
45-degree upward hatch (left to right).

</td>
</tr>
<tr>
<td>
HS_BDIAGONAL

</td>
<td>
45-degree downward hatch (left to right).

</td>
</tr>
<tr>
<td>
HS_CROSS

</td>
<td>
Horizontal and vertical cross hatch.

</td>
</tr>
<tr>
<td>
HS_DIAGCROSS

</td>
<td>
45-degree crosshatch.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>    The number of default hatch patterns that require driver support was reduced in a previous version of the Driver Development Kit (DDK). Consequently, HS_DDI_MAX, typically used by drivers to declare the size of the pattern array, was reduced.</div>
<div> </div>
GDI calls <a href="/windows/desktop/api/winddi/nf-winddi-drvrealizebrush">DrvRealizeBrush</a> with one of these surfaces to realize a brush with a standard pattern.

Each of these surfaces must be a monochrome (1 bit per pixel) GDI bitmap for raster devices. The device driver should choose patterns that will look most like standard patterns when written on the device surface.

GDI is never required to use these brushes in support routines for a vector device. Therefore, surfaces can be device-supported surfaces that <a href="/windows/desktop/api/winddi/nf-winddi-drvrealizebrush">DrvRealizeBrush</a> recognizes as standard patterns.

### -param cjCaps

Specifies the size of the buffer pointed to by <i>pdevcaps</i>. The driver must not access memory beyond the end of the buffer.

### -param pdevcaps [out]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a> structure that will be used to describe device capabilities. GDI zero-initializes this structure calling <b>DrvEnablePDEV</b>.

### -param cjDevInfo

Specifies the number of bytes in the DEVINFO structure pointed to by <i>pdi</i>. The driver should modify no more than this number of bytes in the DEVINFO.

### -param pdi [out]

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure, which describes the driver and the physical device. The driver should only alter the members it understands. GDI fills this structure with zeros before a call to <b>DrvEnablePDEV</b>.

### -param hdev

GDI-supplied handle to the device. This handle must be used as input to some GDI callbacks, such as <a href="/windows/desktop/api/winddi/nf-winddi-enggetdrivername">EngGetDriverName</a>.

### -param pwszDeviceName [in]

Pointer to a null-terminated string that is the user-readable name of the device.

### -param hDriver

Handle to an output device. For a display driver, this is the display device handle. For a printer driver, this parameter should be used as a handle to the printer in calls to the spooler.

## -returns

The return value is a handle to the <a href="/windows-hardware/drivers/">PDEV</a> that identifies the enabled device if the function is successful. That is, <b>DrvEnablePDEV</b> returns a handle to the private, driver-defined device instance information upon success. Otherwise, it returns <b>NULL</b>.

## -remarks

A graphics device driver might support several physical devices attached to different logical addresses. Drivers must also support simultaneous use of different drawing surfaces.

The purposes of <b>DrvEnablePDEV</b> are the following: 

<ol>
<li>
To inform GDI of the physical characteristics of the device.

</li>
<li>
To create a private PDEV structure describing the current device instance (based on the received DEVMODE structure and device name). 

</li>
</ol>
When GDI subsequently calls other graphics DDI functions, it supplies the handle returned by <b>DrvEnablePDEV</b> as input (usually within a SURFOBJ structure) so the driver can identify the device instance.

A single logical device can manage several PDEVs that can be differentiated by the following:

<ol>
<li>
Type of hardware -- A single device driver might support "LaserWhiz," "LaserWhiz II," and "LaserWhiz Super."

</li>
<li>
Logical address -- A single device driver can support printers attached to "LPT1," "COM2," "\SERVER1\PSLAZER," and so forth. A display driver that can support more than one VGA display simultaneously might differentiate them according to port numbers; for example, 0x3CE or 0x2CE.

</li>
<li>
Surfaces -- A printer driver can process two print jobs simultaneously. The two surfaces represent two pages that will be printed. Similarly, a display device driver might support two desktops on the same device.

</li>
</ol>
When receiving a call to this function, the driver must allocate the memory to support the PDEV. However, the actual surface need not be supported until GDI calls <a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a>.

If a device surface requires a bitmap to be allocated, these allocations need not be made until needed. Although applications often request device information long before actually writing to the device, waiting to allocate resources, such as large bitmaps, can conserve memory.

GDI zero-initializes the buffer pointed to by <i>phsurfPatterns</i> before calling this function.

<b>DrvEnablePDEV</b> is required for graphics drivers.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODEW</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvrealizebrush">DrvRealizeBrush</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatepalette">EngCreatePalette</a>



<a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a>