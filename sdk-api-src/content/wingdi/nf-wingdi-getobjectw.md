---
UID: NF:wingdi.GetObjectW
title: GetObjectW function
author: windows-driver-content
description: The GetObject function retrieves information for the specified graphics object.
old-location: gdi\getobject.htm
old-project: gdi
ms.assetid: 555ab876-d990-426d-915c-f98df82a10aa
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetObject, GetObject function [Windows GDI], GetObjectA, GetObjectW, HBITMAP, HBITMAP returned from a call to CreateDIBSection, HBRUSH, HFONT, HPALETTE, HPEN, HPEN returned from a call to ExtCreatePen, _win32_GetObject, gdi.getobject, wingdi/GetObject, wingdi/GetObjectA, wingdi/GetObjectW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-DC-l1-2-0.dll
-	ext-ms-win-gdi-dc-l1-1-0.dll
-	ext-ms-win-gdi-dc-l1-2-1.dll
-	GDI32Full.dll
api_name:
-	GetObject
-	GetObjectA
-	GetObjectW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetObjectW function


## -description


The <b>GetObject</b> function retrieves information for the specified graphics object.


## -parameters




### -param h

TBD


### -param c

TBD


### -param pv

TBD




#### - cbBuffer [in]

The number of bytes of information to be written to the buffer.


#### - hgdiobj [in]

A handle to the graphics object of interest. This can be a handle to one of the following: a logical bitmap, a brush, a font, a palette, a pen, or a device independent bitmap created by calling the <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a> function.


#### - lpvObject [out]

A pointer to a buffer that receives the information about the specified graphics object.

The following table shows the type of information the buffer receives for each type of graphics object you can specify with <i>hgdiobj</i>.

<table>
<tr>
<th>Object type</th>
<th>Data written to buffer</th>
</tr>
<tr>
<td width="40%"><a id="HBITMAP"></a><a id="hbitmap"></a><dl>
<dt><b><b>HBITMAP</b></b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">BITMAP</a>


</td>
</tr>
<tr>
<td width="40%"><a id="HBITMAP_returned_from_a_call_to_CreateDIBSection"></a><a id="hbitmap_returned_from_a_call_to_createdibsection"></a><a id="HBITMAP_RETURNED_FROM_A_CALL_TO_CREATEDIBSECTION"></a><dl>
<dt><b><b>HBITMAP</b> returned from a call to <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a></b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a>, if <i>cbBuffer</i> is set to<code> sizeof (DIBSECTION)</code>, or <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">BITMAP</a>, if <i>cbBuffer</i> is set to <code>sizeof (BITMAP)</code>.

</td>
</tr>
<tr>
<td width="40%"><a id="HPALETTE"></a><a id="hpalette"></a><dl>
<dt><b><b>HPALETTE</b></b></dt>
</dl>
</td>
<td width="60%">
A <b>WORD</b> count of the number of entries in the logical palette

</td>
</tr>
<tr>
<td width="40%"><a id="HPEN_returned_from_a_call_to_ExtCreatePen"></a><a id="hpen_returned_from_a_call_to_extcreatepen"></a><a id="HPEN_RETURNED_FROM_A_CALL_TO_EXTCREATEPEN"></a><dl>
<dt><b><b>HPEN</b> returned from a call to <a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a></b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/34ffa71d-e94d-425e-9f9d-21e3df4990b7">EXTLOGPEN</a>


</td>
</tr>
<tr>
<td width="40%"><a id="HPEN"></a><a id="hpen"></a><dl>
<dt><b><b>HPEN</b></b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/0e098b5a-e249-43ad-a6d8-2509b6562453">LOGPEN</a>


</td>
</tr>
<tr>
<td width="40%"><a id="HBRUSH"></a><a id="hbrush"></a><dl>
<dt><b><b>HBRUSH</b></b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>


</td>
</tr>
<tr>
<td width="40%"><a id="HFONT"></a><a id="hfont"></a><dl>
<dt><b><b>HFONT</b></b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>


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



The buffer pointed to by the <i>lpvObject</i> parameter must be sufficiently large to receive the information about the graphics object. Depending on the graphics object, the function uses a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">BITMAP</a>, <a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a>, <a href="https://msdn.microsoft.com/34ffa71d-e94d-425e-9f9d-21e3df4990b7">EXTLOGPEN</a>, <a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>, <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>, or <a href="https://msdn.microsoft.com/0e098b5a-e249-43ad-a6d8-2509b6562453">LOGPEN</a> structure, or a count of table entries (for a logical palette).

If <i>hgdiobj</i> is a handle to a bitmap created by calling <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>, and the specified buffer is large enough, the <b>GetObject</b> function returns a <a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a> structure. In addition, the <b>bmBits</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">BITMAP</a> structure contained within the <b>DIBSECTION</b> will contain a pointer to the bitmap's bit values.

If <i>hgdiobj</i> is a handle to a bitmap created by any other means, <b>GetObject</b> returns only the width, height, and color format information of the bitmap. You can obtain the bitmap's bit values by calling the <a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a> or <a href="https://msdn.microsoft.com/72e8cc6b-d282-451e-b6ec-0473d2daea7c">GetBitmapBits</a> function.

If <i>hgdiobj</i> is a handle to a logical palette, <b>GetObject</b> retrieves a 2-byte integer that specifies the number of entries in the palette. The function does not retrieve the <a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a> structure defining the palette. To retrieve information about palette entries, an application can call the <a href="https://msdn.microsoft.com/5e72e881-32e1-458e-a09e-91fa13abe178">GetPaletteEntries</a> function.

If <i>hgdiobj</i> is a handle to a font, the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> that is returned is the <b>LOGFONT</b> used to create the font. If Windows had to make some interpolation of the font because the precise <b>LOGFONT</b> could not be represented, the interpolation will not be reflected in the <b>LOGFONT</b>. For example, if you ask for a vertical version of a font that doesn't support vertical painting, the <b>LOGFONT</b> indicates the font is vertical, but Windows will paint it horizontally.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/fc43ab78-c174-400b-a73a-c346d8bda8d2">Storing an Image</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">BITMAP</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/34ffa71d-e94d-425e-9f9d-21e3df4990b7">EXTLOGPEN</a>



<a href="https://msdn.microsoft.com/72e8cc6b-d282-451e-b6ec-0473d2daea7c">GetBitmapBits</a>



<a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>



<a href="https://msdn.microsoft.com/5e72e881-32e1-458e-a09e-91fa13abe178">GetPaletteEntries</a>



<a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a>



<a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>



<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>



<a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a>



<a href="https://msdn.microsoft.com/0e098b5a-e249-43ad-a6d8-2509b6562453">LOGPEN</a>
 

 

