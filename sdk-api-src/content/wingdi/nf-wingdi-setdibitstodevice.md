---
UID: NF:wingdi.SetDIBitsToDevice
title: SetDIBitsToDevice function (wingdi.h)
description: The SetDIBitsToDevice function sets the pixels in the specified rectangle on the device that is associated with the destination device context using color data from a DIB, JPEG, or PNG image.
helpviewer_keywords: ["DIB_PAL_COLORS","DIB_RGB_COLORS","SetDIBitsToDevice","SetDIBitsToDevice function [Windows GDI]","_win32_SetDIBitsToDevice","gdi.setdibitstodevice","wingdi/SetDIBitsToDevice"]
old-location: gdi\setdibitstodevice.htm
tech.root: gdi
ms.assetid: 41225400-12e3-47ba-8b88-ac1d5b0fa90f
ms.date: 12/05/2018
ms.keywords: DIB_PAL_COLORS, DIB_RGB_COLORS, SetDIBitsToDevice, SetDIBitsToDevice function [Windows GDI], _win32_SetDIBitsToDevice, gdi.setdibitstodevice, wingdi/SetDIBitsToDevice
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
 - SetDIBitsToDevice
 - wingdi/SetDIBitsToDevice
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
 - SetDIBitsToDevice
---

# SetDIBitsToDevice function


## -description

The <b>SetDIBitsToDevice</b> function sets the pixels in the specified rectangle on the device that is associated with the destination device context using color data from a DIB, JPEG, or PNG image.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param xDest [in]

The x-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param yDest [in]

The y-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param w [in]

The width, in logical units, of the image.

### -param h [in]

The height, in logical units, of the image.

### -param xSrc [in]

The x-coordinate, in logical units, of the lower-left corner of the image.

### -param ySrc [in]

The y-coordinate, in logical units, of the lower-left corner of the image.

### -param StartScan [in]

The starting scan line in the image.

### -param cLines [in]

The number of DIB scan lines contained in the array pointed to by the <i>lpvBits</i> parameter.

### -param lpvBits [in]

A pointer to the color data stored as an array of bytes. For more information, see the following Remarks section.

### -param lpbmi [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure that contains information about the DIB.

### -param ColorUse [in]

Indicates whether the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure contains explicit red, green, blue (RGB) values or indexes into a palette. For more information, see the following Remarks section.

The <i>fuColorUse</i> parameter must be one of the following values.

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
The color table consists of an array of 16-bit indexes into the currently selected logical palette.

</td>
</tr>
<tr>
<td width="40%"><a id="DIB_RGB_COLORS"></a><a id="dib_rgb_colors"></a><dl>
<dt><b>DIB_RGB_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The color table contains literal RGB values.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the number of scan lines set.

If zero scan lines are set (such as when <i>dwHeight</i> is 0) or the function fails, the function returns zero.

If the driver cannot support the JPEG or PNG file image passed to <b>SetDIBitsToDevice</b>, the function will fail and return GDI_ERROR. If failure does occur, the application must fall back on its own JPEG or PNG support to decompress the image into a bitmap, and then pass the bitmap to <b>SetDIBitsToDevice</b>.

## -remarks

Optimal bitmap drawing speed is obtained when the bitmap bits are indexes into the system palette.

Applications can retrieve the system palette colors and indexes by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getsystempaletteentries">GetSystemPaletteEntries</a> function. After the colors and indexes are retrieved, the application can create the DIB. For more information about the system palette, see <a href="/windows/desktop/gdi/colors">Colors</a>. 

The scan lines must be aligned on a <b>DWORD</b> except for RLE-compressed bitmaps.

The origin of a bottom-up DIB is the lower-left corner of the bitmap; the origin of a top-down DIB is the upper-left corner.

To reduce the amount of memory required to set bits from a large DIB on a device surface, an application can band the output by repeatedly calling <b>SetDIBitsToDevice</b>, placing a different portion of the bitmap into the <i>lpvBits</i> array each time. The values of the <i>uStartScan</i> and <i>cScanLines</i> parameters identify the portion of the bitmap contained in the <i>lpvBits</i> array.

The <b>SetDIBitsToDevice</b> function returns an error if it is called by a process that is running in the background while a full-screen MS-DOS session runs in the foreground.

<ul>
<li>If the <b>biCompression</b> member of <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> is BI_JPEG or BI_PNG, <i>lpvBits</i> points to a buffer containing a JPEG or PNG image. The <b>biSizeImage</b> member of specifies the size of the buffer. The <i>fuColorUse</i> parameter must be set to DIB_RGB_COLORS.</li>
<li>To ensure proper metafile spooling while printing, applications must call the CHECKJPEGFORMAT or CHECKPNGFORMAT escape to verify that the printer recognizes the JPEG or PNG image, respectively, before calling <b>SetDIBitsToDevice</b>.</li>
</ul>
<b>ICM:</b> Color management is performed if color management has been enabled with a call to <a href="/windows/desktop/api/wingdi/nf-wingdi-seticmmode">SetICMMode</a> with the <i>iEnableICM</i> parameter set to ICM_ON. If the bitmap specified by <i>lpbmi</i> has a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv4header">BITMAPV4HEADER</a> that specifies the gamma and endpoints members, or a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header">BITMAPV5HEADER</a> that specifies either the gamma and endpoints members or the profileData and profileSize members, then the call treats the bitmap's pixels as being expressed in the color space described by those members, rather than in the device context's source color space.


#### Examples

For an example, see <a href="/windows/desktop/gdi/testing-a-printer-for-jpeg-or-png-support">Testing a Printer for JPEG or PNG Support</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getsystempaletteentries">GetSystemPaletteEntries</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>