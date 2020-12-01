---
UID: NF:winddi.DrvCreateDeviceBitmap
title: DrvCreateDeviceBitmap function (winddi.h)
description: The DrvCreateDeviceBitmap function creates and manages bitmaps.
helpviewer_keywords: ["DrvCreateDeviceBitmap","DrvCreateDeviceBitmap function [Display Devices]","ddifncs_b3a739da-4a9d-4e84-a4e8-8b1e790a06af.xml","display.drvcreatedevicebitmap","winddi/DrvCreateDeviceBitmap"]
old-location: display\drvcreatedevicebitmap.htm
tech.root: display
ms.assetid: 1f5f49ef-bf08-4311-9a1b-fdc37e6c2063
ms.date: 12/05/2018
ms.keywords: DrvCreateDeviceBitmap, DrvCreateDeviceBitmap function [Display Devices], ddifncs_b3a739da-4a9d-4e84-a4e8-8b1e790a06af.xml, display.drvcreatedevicebitmap, winddi/DrvCreateDeviceBitmap
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
 - DrvCreateDeviceBitmap
 - winddi/DrvCreateDeviceBitmap
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
 - DrvCreateDeviceBitmap
---

# DrvCreateDeviceBitmap function


## -description

The <b>DrvCreateDeviceBitmap</b> function creates and manages bitmaps.

## -parameters

### -param dhpdev

Handle to the PDEV that describes the physical device that an application has designated as the primary target for a bitmap. The format of the bitmap must be compatible with this physical device.

### -param sizl

Specifies a SIZEL structure that contains the width and height of the bitmap to be created. The <b>cx</b> and <b>cy</b> members of this structure contain respectively, the bitmap's width and height, in pixels. A SIZEL structure is identical to a <a href="/windows/desktop/api/windef/ns-windef-size">SIZE</a> structure.

### -param iFormat

Specifies the bitmap format, which indicates the required number of bits of color information per pixel, and always matches the format of the primary. This value can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BMF_8BPP

</td>
<td>
8 bits per pixel.

</td>
</tr>
<tr>
<td>
BMF_16BPP

</td>
<td>
16 bits per pixel.

</td>
</tr>
<tr>
<td>
BMF_24BPP

</td>
<td>
24 bits per pixel.

</td>
</tr>
<tr>
<td>
BMF_32BPP

</td>
<td>
32 bits per pixel.

</td>
</tr>
</table>

## -returns

The return value is a handle that identifies the created bitmap if the function is successful. If the driver chooses to let GDI create and manage the bitmap, the return value is zero. If an error occurs, the return value is 0xFFFFFFFF, and GDI logs an error code.

## -remarks

If the driver creates the bitmap, it can store it anywhere and in any format. It is assumed that the driver will take into account the specifications of the parameters and provide a bitmap with at least as many bits per pixel as requested.

The contents of the created bitmap are undefined.

This function is optional. If this function is implemented, however, <a href="/windows/desktop/api/winddi/nf-winddi-drvdeletedevicebitmap">DrvDeleteDeviceBitmap</a> must also be implemented.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvdeletedevicebitmap">DrvDeleteDeviceBitmap</a>