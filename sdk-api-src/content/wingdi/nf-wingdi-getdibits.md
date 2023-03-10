---
UID: NF:wingdi.GetDIBits
title: GetDIBits function (wingdi.h)
description: The GetDIBits function retrieves the bits of the specified compatible bitmap and copies them into a buffer as a DIB using the specified format.
helpviewer_keywords: ["DIB_PAL_COLORS","DIB_RGB_COLORS","GetDIBits","GetDIBits function [Windows GDI]","_win32_GetDIBits","gdi.getdibits","wingdi/GetDIBits"]
old-location: gdi\getdibits.htm
tech.root: gdi
ms.assetid: be3ffa3f-b343-4e38-8b1e-aeccf35d92b8
ms.date: 12/05/2018
ms.keywords: DIB_PAL_COLORS, DIB_RGB_COLORS, GetDIBits, GetDIBits function [Windows GDI], _win32_GetDIBits, gdi.getdibits, wingdi/GetDIBits
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
 - GetDIBits
 - wingdi/GetDIBits
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
 - GetDIBits
---

# GetDIBits function


## -description

The <b>GetDIBits</b> function retrieves the bits of the specified compatible bitmap and copies them into a buffer as a DIB using the specified format.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param hbm [in]

A handle to the bitmap. This must be a compatible bitmap (DDB).

### -param start [in]

The first scan line to retrieve.

### -param cLines [in]

The number of scan lines to retrieve.

### -param lpvBits [out]

A pointer to a buffer to receive the bitmap data. If this parameter is <b>NULL</b>, the function passes the dimensions and format of the bitmap to the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure pointed to by the <i>lpbmi</i> parameter.

### -param lpbmi [in, out]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure that specifies the desired format for the DIB data.

### -param usage [in]

The format of the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure. It must be one of the following values.

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
The color table should consist of an array of 16-bit indexes into the current logical palette.

</td>
</tr>
<tr>
<td width="40%"><a id="DIB_RGB_COLORS"></a><a id="dib_rgb_colors"></a><dl>
<dt><b>DIB_RGB_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The color table should consist of literal red, green, blue (RGB) values.

</td>
</tr>
</table>

## -returns

If the <i>lpvBits</i> parameter is non-<b>NULL</b> and the function succeeds, the return value is the number of scan lines copied from the bitmap.

If the <i>lpvBits</i> parameter is <b>NULL</b> and <b>GetDIBits</b> successfully fills the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure, the return value is nonzero.

If the function fails, the return value is zero.

This function can return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters is invalid.

</td>
</tr>
</table>

## -remarks

If the requested format for the DIB matches its internal format, the RGB values for the bitmap are copied. If the requested format doesn't match the internal format, a color table is synthesized. The following table describes the color table synthesized for each format.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>1_BPP</td>
<td>The color table consists of a black and a white entry.</td>
</tr>
<tr>
<td>4_BPP</td>
<td>The color table consists of a mix of colors identical to the standard VGA palette.</td>
</tr>
<tr>
<td>8_BPP</td>
<td>The color table consists of a general mix of 256 colors defined by GDI. (Included in these 256 colors are the 20 colors found in the default logical palette.)</td>
</tr>
<tr>
<td>24_BPP</td>
<td>No color table is returned.</td>
</tr>
</table>
 

If the <i>lpvBits</i> parameter is a valid pointer, the first six members of the <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure must be initialized to specify the size and format of the DIB. The scan lines must be aligned on a <b>DWORD</b> except for RLE compressed bitmaps.

A bottom-up DIB is specified by setting the height to a positive number, while a top-down DIB is specified by setting the height to a negative number. The bitmap color table will be appended to the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

If <i>lpvBits</i> is <b>NULL</b>, <b>GetDIBits</b> examines the first member of the first structure pointed to by <i>lpbi</i>. This member must specify the size, in bytes, of a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreheader">BITMAPCOREHEADER</a> or a <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure. The function uses the specified size to determine how the remaining members should be initialized.

If <i>lpvBits</i> is <b>NULL</b> and the bit count member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is initialized to zero, <b>GetDIBits</b> fills in a <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure or <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreheader">BITMAPCOREHEADER</a> without the color table. This technique can be used to query bitmap attributes.

The bitmap identified by the <i>hbmp</i> parameter must not be selected into a device context when the application calls this function.

The origin for a bottom-up DIB is the lower-left corner of the bitmap; the origin for a top-down DIB is the upper-left corner.


#### Examples

For an example, see <a href="/windows/desktop/gdi/capturing-an-image">Capturing an Image</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreheader">BITMAPCOREHEADER</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>
