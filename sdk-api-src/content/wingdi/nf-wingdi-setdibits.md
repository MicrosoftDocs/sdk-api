---
UID: NF:wingdi.SetDIBits
title: SetDIBits function (wingdi.h)
description: The SetDIBits function sets the pixels in a compatible bitmap (DDB) using the color data found in the specified DIB.
helpviewer_keywords: ["DIB_PAL_COLORS","DIB_RGB_COLORS","SetDIBits","SetDIBits function [Windows GDI]","_win32_SetDIBits","gdi.setdibits","wingdi/SetDIBits"]
old-location: gdi\setdibits.htm
tech.root: gdi
ms.assetid: 706f4532-4073-4d5c-ae2d-e33aea9163e9
ms.date: 12/05/2018
ms.keywords: DIB_PAL_COLORS, DIB_RGB_COLORS, SetDIBits, SetDIBits function [Windows GDI], _win32_SetDIBits, gdi.setdibits, wingdi/SetDIBits
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
 - SetDIBits
 - wingdi/SetDIBits
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
 - SetDIBits
---

# SetDIBits function


## -description

The <b>SetDIBits</b> function sets the pixels in a compatible bitmap (DDB) using the color data found in the specified DIB.

## -parameters

### -param hdc [in]

A handle to a device context.

### -param hbm [in]

A handle to the compatible bitmap (DDB) that is to be altered using the color data from the specified DIB.

### -param start [in]

The starting scan line for the device-independent color data in the array pointed to by the <i>lpvBits</i> parameter.

### -param cLines [in]

The number of scan lines found in the array containing device-independent color data.

### -param lpBits [in]

A pointer to the DIB color data, stored as an array of bytes. The format of the bitmap values depends on the <b>biBitCount</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure pointed to by the <i>lpbmi</i> parameter.

### -param lpbmi [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure that contains information about the DIB.

### -param ColorUse [in]

Indicates whether the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure was provided and, if so, whether <b>bmiColors</b> contains explicit red, green, blue (RGB) values or palette indexes. The <i>fuColorUse</i> parameter must be one of the following values.

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
The color table consists of an array of 16-bit indexes into the logical palette of the device context identified by the <i>hdc</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="DIB_RGB_COLORS"></a><a id="dib_rgb_colors"></a><dl>
<dt><b>DIB_RGB_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The color table is provided and contains literal RGB values.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the number of scan lines copied.

If the function fails, the return value is zero.

This can be the following value.

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

Optimal bitmap drawing speed is obtained when the bitmap bits are indexes into the system palette.

Applications can retrieve the system palette colors and indexes by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getsystempaletteentries">GetSystemPaletteEntries</a> function. After the colors and indexes are retrieved, the application can create the DIB. For more information, see <a href="/windows/desktop/gdi/system-palette">System Palette</a>.

The device context identified by the <i>hdc</i> parameter is used only if the DIB_PAL_COLORS constant is set for the <i>fuColorUse</i> parameter; otherwise it is ignored.

The bitmap identified by the <i>hbmp</i> parameter must not be selected into a device context when the application calls this function.

The scan lines must be aligned on a <b>DWORD</b> except for RLE-compressed bitmaps.

The origin for bottom-up DIBs is the lower-left corner of the bitmap; the origin for top-down DIBs is the upper-left corner of the bitmap.

<b>ICM:</b> Color management is performed if color management has been enabled with a call to <a href="/windows/desktop/api/wingdi/nf-wingdi-seticmmode">SetICMMode</a> with the <i>iEnableICM</i> parameter set to ICM_ON. If the bitmap specified by <i>lpbmi</i> has a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv4header">BITMAPV4HEADER</a> that specifies the gamma and endpoints members, or a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header">BITMAPV5HEADER</a> that specifies either the gamma and endpoints members or the profileData and profileSize members, then the call treats the bitmap's pixels as being expressed in the color space described by those members, rather than in the device context's source color space.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getsystempaletteentries">GetSystemPaletteEntries</a>