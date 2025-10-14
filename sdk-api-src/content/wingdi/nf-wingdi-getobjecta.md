---
UID: NF:wingdi.GetObjectA
title: GetObjectA function (wingdi.h)
description: The GetObject function retrieves information for the specified graphics object. (GetObjectA)
helpviewer_keywords: ["GetObjectA", "HBITMAP", "HBITMAP returned from a call to CreateDIBSection", "HBRUSH", "HFONT", "HPALETTE", "HPEN", "HPEN returned from a call to ExtCreatePen", "wingdi/GetObjectA"]
old-location: gdi\getobject.htm
tech.root: gdi
ms.assetid: 555ab876-d990-426d-915c-f98df82a10aa
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject function [Windows GDI], GetObjectA, GetObjectW, HBITMAP, HBITMAP returned from a call to CreateDIBSection, HBRUSH, HFONT, HPALETTE, HPEN, HPEN returned from a call to ExtCreatePen, _win32_GetObject, gdi.getobject, wingdi/GetObject, wingdi/GetObjectA, wingdi/GetObjectW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetObjectW (Unicode) and GetObjectA (ANSI)
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
 - GetObjectA
 - wingdi/GetObjectA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-l1-2-0.dll
 - ext-ms-win-gdi-dc-l1-1-0.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - GetObject
 - GetObjectA
 - GetObjectW
---

# GetObjectA function


## -description

The <b>GetObject</b> function retrieves information for the specified graphics object.

## -parameters

### -param hgdiobj [in]

A handle to the graphics object of interest. This can be a handle to one of the following: a logical bitmap, a brush, a font, a palette, a pen, or a device independent bitmap created by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a> function.

### -param cbBuffer [in]

The number of bytes of information to be written to the buffer.

### -param lpvObject [out]

A pointer to a buffer that receives the information about the specified graphics object.

The following table shows the type of information the buffer receives for each type of graphics object you can specify with <i>hgdiobj</i>.

<table>
<tr>
<th>Object type</th>
<th>Data written to buffer</th>
</tr>
<tr>
<td width="40%"><a id="HBITMAP"></a><a id="hbitmap"></a><dl>
<dt><b>HBITMAP</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a>


</td>
</tr>
<tr>
<td width="40%"><a id="HBITMAP_returned_from_a_call_to_CreateDIBSection"></a><a id="hbitmap_returned_from_a_call_to_createdibsection"></a><a id="HBITMAP_RETURNED_FROM_A_CALL_TO_CREATEDIBSECTION"></a><dl>
<dt><b>HBITMAP returned from a call to <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a></b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a>, if <i>cbBuffer</i> is set to<code> sizeof (DIBSECTION)</code>, or <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a>, if <i>cbBuffer</i> is set to <code>sizeof (BITMAP)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="HPALETTE"></a><a id="hpalette"></a><dl>
<dt><b>HPALETTE</b></dt>
</dl>
</td>
<td width="60%">
A <b>WORD</b> count of the number of entries in the logical palette

</td>
</tr>
<tr>
<td width="40%"><a id="HPEN_returned_from_a_call_to_ExtCreatePen"></a><a id="hpen_returned_from_a_call_to_extcreatepen"></a><a id="HPEN_RETURNED_FROM_A_CALL_TO_EXTCREATEPEN"></a><dl>
<dt><b>HPEN returned from a call to <a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a></b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/ns-wingdi-extlogpen">EXTLOGPEN</a>


</td>
</tr>
<tr>
<td width="40%"><a id="HPEN"></a><a id="hpen"></a><dl>
<dt><b>HPEN</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/ns-wingdi-logpen">LOGPEN</a>


</td>
</tr>
<tr>
<td width="40%"><a id="HBRUSH"></a><a id="hbrush"></a><dl>
<dt><b>HBRUSH</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a>


</td>
</tr>
<tr>
<td width="40%"><a id="HFONT"></a><a id="hfont"></a><dl>
<dt><b>HFONT</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>


</td>
</tr>
</table>
 

If the <i>lpvObject</i> parameter is <b>NULL</b>, the function return value is the number of bytes required to store the information it writes to the buffer for the specified graphics object.

The address of <i>lpvObject</i> must be on a 4-byte boundary; otherwise, <b>GetObject</b> fails.

## -returns

If the function succeeds, and <i>lpvObject</i> is a valid pointer, the return value is the number of bytes stored into the buffer.

If the function succeeds, and <i>lpvObject</i> is <b>NULL</b>, the return value is the number of bytes required to hold the information the function would store into the buffer.

If the function fails, the return value is zero.

## -remarks

The buffer pointed to by the <i>lpvObject</i> parameter must be sufficiently large to receive the information about the graphics object. Depending on the graphics object, the function uses a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a>, <a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a>, <a href="/windows/desktop/api/wingdi/ns-wingdi-extlogpen">EXTLOGPEN</a>, <a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a>, <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>, or <a href="/windows/desktop/api/wingdi/ns-wingdi-logpen">LOGPEN</a> structure, or a count of table entries (for a logical palette).

If <i>hgdiobj</i> is a handle to a bitmap created by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>, and the specified buffer is large enough, the <b>GetObject</b> function returns a <a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a> structure. In addition, the <b>bmBits</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a> structure contained within the <b>DIBSECTION</b> will contain a pointer to the bitmap's bit values.

If <i>hgdiobj</i> is a handle to a bitmap created by any other means, <b>GetObject</b> returns only the width, height, and color format information of the bitmap. You can obtain the bitmap's bit values by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-getbitmapbits">GetBitmapBits</a> function.

If <i>hgdiobj</i> is a handle to a logical palette, <b>GetObject</b> retrieves a 2-byte integer that specifies the number of entries in the palette. The function does not retrieve the <a href="/windows/desktop/api/wingdi/ns-wingdi-logpalette">LOGPALETTE</a> structure defining the palette. To retrieve information about palette entries, an application can call the <a href="/windows/desktop/api/wingdi/nf-wingdi-getpaletteentries">GetPaletteEntries</a> function.

If <i>hgdiobj</i> is a handle to a font, the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> that is returned is the <b>LOGFONT</b> used to create the font. If Windows had to make some interpolation of the font because the precise <b>LOGFONT</b> could not be represented, the interpolation will not be reflected in the <b>LOGFONT</b>. For example, if you ask for a vertical version of a font that doesn't support vertical painting, the <b>LOGFONT</b> indicates the font is vertical, but Windows will paint it horizontally.


#### Examples

For an example, see <a href="/windows/desktop/gdi/storing-an-image">Storing an Image</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines GetObject as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-extlogpen">EXTLOGPEN</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbitmapbits">GetBitmapBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getpaletteentries">GetPaletteEntries</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logpalette">LOGPALETTE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logpen">LOGPEN</a>
