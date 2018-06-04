---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# GetDIBits function


## -description


The <b>GetDIBits</b> function retrieves the bits of the specified compatible bitmap and copies them into a buffer as a DIB using the specified format.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param hbm

TBD


### -param start

TBD


### -param cLines

TBD


### -param lpvBits [out]

A pointer to a buffer to receive the bitmap data. If this parameter is <b>NULL</b>, the function passes the dimensions and format of the bitmap to the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure pointed to by the <i>lpbi</i> parameter.


### -param lpbmi

TBD


### -param usage

TBD




#### - cScanLines [in]

The number of scan lines to retrieve.


#### - hbmp [in]

A handle to the bitmap. This must be a compatible bitmap (DDB).


#### - lpbi [in, out]

A pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure that specifies the desired format for the DIB data.


#### - uStartScan [in]

The first scan line to retrieve.


#### - uUsage [in]

The format of the <b>bmiColors</b> member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure. It must be one of the following values.

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

If the <i>lpvBits</i> parameter is <b>NULL</b> and <b>GetDIBits</b> successfully fills the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure, the return value is nonzero.

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
 

If the <i>lpvBits</i> parameter is a valid pointer, the first six members of the <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure must be initialized to specify the size and format of the DIB. The scan lines must be aligned on a <b>DWORD</b> except for RLE compressed bitmaps.

A bottom-up DIB is specified by setting the height to a positive number, while a top-down DIB is specified by setting the height to a negative number. The bitmap color table will be appended to the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.

If <i>lpvBits</i> is <b>NULL</b>, <b>GetDIBits</b> examines the first member of the first structure pointed to by <i>lpbi</i>. This member must specify the size, in bytes, of a <a href="https://msdn.microsoft.com/0182adcd-dbba-43de-b41b-ab2f0fd8f7bf">BITMAPCOREHEADER</a> or a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure. The function uses the specified size to determine how the remaining members should be initialized.

If <i>lpvBits</i> is <b>NULL</b> and the bit count member of <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> is initialized to zero, <b>GetDIBits</b> fills in a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure or <a href="https://msdn.microsoft.com/0182adcd-dbba-43de-b41b-ab2f0fd8f7bf">BITMAPCOREHEADER</a> without the color table. This technique can be used to query bitmap attributes.

The bitmap identified by the <i>hbmp</i> parameter must not be selected into a device context when the application calls this function.

The origin for a bottom-up DIB is the lower-left corner of the bitmap; the origin for a top-down DIB is the upper-left corner.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/672fc2e4-c35c-4d5d-98fa-85f2ad56d9b0">Capturing an Image</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0182adcd-dbba-43de-b41b-ab2f0fd8f7bf">BITMAPCOREHEADER</a>



<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>
 

 

