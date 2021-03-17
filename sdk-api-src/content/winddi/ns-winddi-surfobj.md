---
UID: NS:winddi._SURFOBJ
title: SURFOBJ (winddi.h)
description: The SURFOBJ structure is the user object for a surface. A device driver usually calls methods on a surface object only when the surface object represents a GDI bitmap or a device-managed surface.
helpviewer_keywords: ["SURFOBJ","SURFOBJ structure [Display Devices]","display.surfobj","grstrcts_ef22095d-660f-4276-9a10-1ce7451327fc.xml","winddi/SURFOBJ"]
old-location: display\surfobj.htm
tech.root: display
ms.assetid: cee7cb50-1e8a-422b-aebe-7030ae96fb34
ms.date: 12/05/2018
ms.keywords: SURFOBJ, SURFOBJ structure [Display Devices], display.surfobj, grstrcts_ef22095d-660f-4276-9a10-1ce7451327fc.xml, winddi/SURFOBJ
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.typenames: SURFOBJ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SURFOBJ
 - winddi/_SURFOBJ
 - SURFOBJ
 - winddi/SURFOBJ
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
 - SURFOBJ
---

# SURFOBJ structure


## -description

The SURFOBJ structure is the user object for a surface. A device driver usually calls methods on a surface object only when the surface object represents a GDI bitmap or a <a href="/windows-hardware/drivers/">device-managed surface</a>.

## -struct-fields

### -field dhsurf

Handle to a surface, provided that the surface is device-managed. Otherwise, this member is zero.

### -field hsurf

Handle to the surface.

### -field dhpdev

Identifies the device's <a href="/windows-hardware/drivers/">PDEV</a> that is associated with the specified surface.

### -field hdev

GDI's logical handle to the PDEV associated with this device.

### -field sizlBitmap

Specifies a SIZEL structure that contains the width and height, in pixels, of the surface. The SIZEL structure is identical to the <a href="/windows/desktop/api/windef/ns-windef-size">SIZE</a> structure.

### -field cjBits

Specifies the size of the buffer pointed to by <b>pvBits</b>.

### -field pvBits

If the surface is a standard format bitmap, this is a pointer to the surface's pixels. For BMF_JPEG or BMF_PNG images, this is a pointer to a buffer containing the image data in a JPEG or PNG format. Otherwise, this member is <b>NULL</b>.

### -field pvScan0

Pointer to the first scan line of the bitmap. If <b>iBitmapFormat</b> is BMF_JPEG or BMF_PNG, this member is <b>NULL</b>.

### -field lDelta

Specifies the count of bytes required to move down one scan line in the bitmap. If <b>iBitmapFormat</b> is BMF_JPEG or BMF_PNG, this member is <b>NULL</b>.

### -field iUniq

Specifies the current state of the specified surface. Every time the surface changes, this value is incremented. This enables drivers to cache source surfaces.

For a surface that should not be cached, <b>iUniq</b> is set to zero. This value is used in conjunction with the BMF_DONTCACHE flag of <b>fjBitmap</b>.

### -field iBitmapFormat

Specifies the standard format most closely matching this surface. If the <b>iType</b> member specifies a bitmap (STYPE_BITMAP), this member specifies its format. NT-based operating systems support a set of predefined formats, although applications can also send device-specific formats by using <b>SetDIBitsToDevice</b>. Supported predefined formats include the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BMF_1BPP

</td>
<td>
1 bit per pixel.

</td>
</tr>
<tr>
<td>
BMF_4BPP

</td>
<td>
4 bits per pixel.

</td>
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
<tr>
<td>
BMF_4RLE

</td>
<td>
4 bits per pixel, run length encoded.

</td>
</tr>
<tr>
<td>
BMF_8RLE

</td>
<td>
8 bits per pixel, run length encoded.

</td>
</tr>
<tr>
<td>
BMF_JPEG

</td>
<td>
JPEG compressed image.

</td>
</tr>
<tr>
<td>
BMF_PNG

</td>
<td>
PNG compressed image.

</td>
</tr>
</table>

### -field iType

Surface type, which is one of the following:

<table>
<tr>
<th>Type</th>
<th>Definition</th>
</tr>
<tr>
<td>
STYPE_BITMAP

</td>
<td>
The surface is a bitmap.

</td>
</tr>
<tr>
<td>
STYPE_DEVBITMAP

</td>
<td>
The surface is a device format bitmap.

</td>
</tr>
<tr>
<td>
STYPE_DEVICE

</td>
<td>
The surface is managed by the device.

</td>
</tr>
</table>

### -field fjBitmap

If the surface is of type STYPE_BITMAP and is a standard uncompressed format bitmap, the following flags can be set. Otherwise, this member should be ignored.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BMF_DONTCACHE

</td>
<td>
The bitmap should not be cached by the driver because it is a transient bitmap, created by GDI, that the driver will never see again. If this flag is set, the <b>iUniq</b> member of this structure will be set to 0.

</td>
</tr>
<tr>
<td>
BMF_KMSECTION

</td>
<td>
Is used by GDI only and should be ignored by the driver. 

</td>
</tr>
<tr>
<td>
BMF_NOTSYSMEM

</td>
<td>
The bitmap is not in system memory. <a href="/windows/desktop/api/winddi/nf-winddi-engmodifysurface">EngModifySurface</a> sets this flag when it moves a bitmap into video memory.

</td>
</tr>
<tr>
<td>
BMF_NOZEROINIT

</td>
<td>
The bitmap was not zero-initialized.

</td>
</tr>
<tr>
<td>
BMF_TOPDOWN

</td>
<td>
The first scan line represents the <i>top</i> of the bitmap.

</td>
</tr>
<tr>
<td>
BMF_WINDOW_BLT

</td>
<td>
GDI sets this flag to notify the driver of a window move from one screen location to another.  

</td>
</tr>
</table>

## -remarks

When information about a particular surface is required by a driver, the driver must access the SURFOBJ. This structure allows quick access to the properties of the surface.

When a SURFOBJ structure represents a GDI bitmap, the driver must be able to determine the format of the bitmap and locate the bitmap bits.

When a SURFOBJ structure represents a device surface, the driver must be able to locate the device handle for the surface.

For more information about supporting JPEG and PNG compressed images, see <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>.