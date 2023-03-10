---
UID: NF:wingdi.StretchDIBits
title: StretchDIBits function (wingdi.h)
description: The StretchDIBits function copies the color data for a rectangle of pixels in a DIB, JPEG, or PNG image to the specified destination rectangle.
helpviewer_keywords: ["DIB_PAL_COLORS","DIB_RGB_COLORS","StretchDIBits","StretchDIBits function [Windows GDI]","_win32_StretchDIBits","gdi.stretchdibits","wingdi/StretchDIBits"]
old-location: gdi\stretchdibits.htm
tech.root: gdi
ms.assetid: 3d57a79a-338d-48ab-8161-3ce17739bf20
ms.date: 12/05/2018
ms.keywords: DIB_PAL_COLORS, DIB_RGB_COLORS, StretchDIBits, StretchDIBits function [Windows GDI], _win32_StretchDIBits, gdi.stretchdibits, wingdi/StretchDIBits
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
 - StretchDIBits
 - wingdi/StretchDIBits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - StretchDIBits
---

# StretchDIBits function


## -description

The <b>StretchDIBits</b> function copies the color data for a rectangle of pixels in a DIB, JPEG, or PNG image to the specified destination rectangle. If the destination rectangle is larger than the source rectangle, this function stretches the rows and columns of color data to fit the destination rectangle. If the destination rectangle is smaller than the source rectangle, this function compresses the rows and columns by using the specified raster operation.

## -parameters

### -param hdc [in]

A handle to the destination device context.

### -param xDest [in]

The x-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param yDest [in]

The y-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param DestWidth [in]

The width, in logical units, of the destination rectangle.

### -param DestHeight [in]

The height, in logical units, of the destination rectangle.

### -param xSrc [in]

The x-coordinate, in pixels, of the source rectangle in the image.

### -param ySrc [in]

The y-coordinate, in pixels, of the source rectangle in the image.

### -param SrcWidth [in]

The width, in pixels, of the source rectangle in the image.

### -param SrcHeight [in]

The height, in pixels, of the source rectangle in the image.

### -param lpBits [in]

A pointer to the image bits, which are stored as an array of bytes. For more information, see the Remarks section.

### -param lpbmi [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure that contains information about the DIB.

### -param iUsage [in]

Specifies whether the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure was provided and, if so, whether <b>bmiColors</b> contains explicit red, green, blue (RGB) values or indexes. The <i>iUsage</i> parameter must be one of the following values.

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
The array contains 16-bit indexes into the logical palette of the source device context.

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
 

For more information, see the Remarks section.

### -param rop [in]

A raster-operation code that specifies how the source pixels, the destination device context's current brush, and the destination pixels are to be combined to form the new image. For a list of some common raster operation codes, see <a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a>.

## -returns

If the function succeeds, the return value is the number of scan lines copied. Note that this value can be negative for mirrored content.

If the function fails, or no scan lines are copied, the return value is 0.

If the driver cannot support the JPEG or PNG file image passed to <b>StretchDIBits</b>, the function will fail and return GDI_ERROR. If failure does occur, the application must fall back on its own JPEG or PNG support to decompress the image into a bitmap, and then pass the bitmap to <b>StretchDIBits</b>.

## -remarks

The origin of a bottom-up DIB is the lower-left corner; the origin of a top-down DIB is the upper-left corner.

<b>StretchDIBits</b> creates a mirror image of a bitmap if the signs of the <i>nSrcWidth</i> and <i>nDestWidth</i> parameters, or if the <i>nSrcHeight</i> and <i>nDestHeight</i> parameters differ. If <i>nSrcWidth</i> and <i>nDestWidth</i> have different signs, the function creates a mirror image of the bitmap along the x-axis. If <i>nSrcHeight</i> and <i>nDestHeight</i> have different signs, the function creates a mirror image of the bitmap along the y-axis.

<b>StretchDIBits</b> creates a top-down image if the sign of the <b>biHeight</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure for the DIB is negative. For a code example, see <a href="/windows/desktop/gdi/sizing-a-jpeg-or-png-image">Sizing a JPEG or PNG Image</a>.

This function allows a JPEG or PNG image to be passed as the source image. How each parameter is used remains the same, except:

<ul>
<li>If the <b>biCompression</b> member of <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> is BI_JPEG or BI_PNG, <i>lpBits</i> points to a buffer containing a JPEG or PNG image, respectively. The <b>biSizeImage</b> member of the <b>BITMAPINFOHEADER</b> structure specifies the size of the buffer. The <i>iUsage</i> parameter must be set to DIB_RGB_COLORS. The <i>dwRop</i> parameter must be set to SRCCOPY.</li>
<li>To ensure proper metafile spooling while printing, applications must call the CHECKJPEGFORMAT or CHECKPNGFORMAT escape to verify that the printer recognizes the JPEG or PNG image, respectively, before calling <b>StretchDIBits</b>.</li>
</ul>
<b>ICM:</b> Color management is performed if color management has been enabled with a call to <a href="/windows/desktop/api/wingdi/nf-wingdi-seticmmode">SetICMMode</a> with the <i>iEnableICM</i> parameter set to ICM_ON. If the bitmap specified by <i>lpBitsInfo</i> has a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv4header">BITMAPV4HEADER</a> that specifies the gamma and endpoints members, or a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header">BITMAPV5HEADER</a> that specifies either the gamma and endpoints members or the profileData and profileSize members, then the call treats the bitmap's pixels as being expressed in the color space described by those members, rather than in the device context's source color space.


#### Examples

For an example, see <a href="/windows/desktop/gdi/sizing-a-jpeg-or-png-image">Sizing a JPEG or PNG Image</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO
      </a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setmapmode">SetMapMode
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode
      </a>