---
UID: NF:wingdi.CreateDIBitmap
title: CreateDIBitmap function (wingdi.h)
description: The CreateDIBitmap function creates a compatible bitmap (DDB) from a DIB and, optionally, sets the bitmap bits.
helpviewer_keywords: ["CBM_INIT","CreateDIBitmap","CreateDIBitmap function [Windows GDI]","DIB_PAL_COLORS","DIB_RGB_COLORS","_win32_CreateDIBitmap","gdi.createdibitmap","wingdi/CreateDIBitmap"]
old-location: gdi\createdibitmap.htm
tech.root: gdi
ms.assetid: e9a5b525-a6b6-4309-9e53-69d274b85783
ms.date: 12/05/2018
ms.keywords: CBM_INIT, CreateDIBitmap, CreateDIBitmap function [Windows GDI], DIB_PAL_COLORS, DIB_RGB_COLORS, _win32_CreateDIBitmap, gdi.createdibitmap, wingdi/CreateDIBitmap
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateDIBitmap
 - wingdi/CreateDIBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - CreateDIBitmap
---

# CreateDIBitmap function


## -description

The <b>CreateDIBitmap</b> function creates a compatible bitmap (DDB) from a DIB and, optionally, sets the bitmap bits.

## -parameters

### -param hdc [in]

A handle to a device context.

### -param pbmih [in]

A pointer to a bitmap information header structure, <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header">BITMAPV5HEADER</a>.

If <i>fdwInit</i> is CBM_INIT, the function uses the bitmap information header structure to obtain the desired width and height of the bitmap as well as other information. Note that a positive value for the height indicates a bottom-up DIB while a negative value for the height indicates a top-down DIB. Calling <b>CreateDIBitmap</b> with <i>fdwInit</i> as CBM_INIT is equivalent to calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a> function to create a DDB in the format of the device and then calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> function to translate the DIB bits to the DDB.

### -param flInit [in]

Specifies how the system initializes the bitmap bits. The following value is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CBM_INIT"></a><a id="cbm_init"></a><dl>
<dt><b>CBM_INIT</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system uses the data pointed to by the <i>lpbInit</i> and <i>lpbmi</i> parameters to initialize the bitmap bits.

If this flag is clear, the data pointed to by those parameters is not used.

</td>
</tr>
</table>
 

If <i>fdwInit</i> is zero, the system does not initialize the bitmap bits.

### -param pjBits [in]

A pointer to an array of bytes containing the initial bitmap data. The format of the data depends on the <b>biBitCount</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure to which the <i>lpbmi</i> parameter points.

### -param pbmi [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure that describes the dimensions and color format of the array pointed to by the <i>lpbInit</i> parameter.

### -param iUsage [in]

Specifies whether the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure was initialized and, if so, whether <b>bmiColors</b> contains explicit red, green, blue (RGB) values or palette indexes. The <i>fuUsage</i> parameter must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DIB_PAL_COLORS"></a><a id="dib_pal_colors"></a><dl>
<dt><b>DIB_PAL_COLORS</b></dt>
</dl>
</td>
<td width="60%">
A color table is provided and consists of an array of 16-bit indexes into the logical palette of the device context into which the bitmap is to be selected.

</td>
</tr>
<tr>
<td width="40%"><a id="DIB_RGB_COLORS"></a><a id="dib_rgb_colors"></a><dl>
<dt><b>DIB_RGB_COLORS</b></dt>
</dl>
</td>
<td width="60%">
A color table is provided and contains literal RGB values.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a handle to the compatible bitmap.

If the function fails, the return value is <b>NULL</b>.

## -remarks

The DDB that is created will be whatever bit depth your reference DC is. To create a bitmap that is of different bit depth, use <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>.

For a device to reach optimal bitmap-drawing speed, specify <i>fdwInit</i> as CBM_INIT. Then, use the same color depth DIB as the video mode. When the video is running 4- or 8-bpp, use DIB_PAL_COLORS.

The CBM_CREATDIB flag for the <i>fdwInit</i> parameter is no longer supported.

When you no longer need the bitmap, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

<b>ICM:</b> No color management is performed. The contents of the resulting bitmap are not color matched after the bitmap has been created.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getsystempaletteentries">GetSystemPaletteEntries</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>