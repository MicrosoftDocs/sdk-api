---
UID: NS:wingdi.tagBITMAPCOREINFO
title: tagBITMAPCOREINFO
author: windows-sdk-content
description: The BITMAPCOREINFO structure defines the dimensions and color information for a DIB.
old-location: gdi\bitmapcoreinfo.htm
tech.root: gdi
ms.assetid: cb6cb9da-8f7f-47e9-980a-aa77fe04c80c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPBITMAPCOREINFO, *PBITMAPCOREINFO, BITMAPCOREINFO, BITMAPCOREINFO structure [Windows GDI], PBITMAPCOREINFO, PBITMAPCOREINFO structure pointer [Windows GDI], _win32_BITMAPCOREINFO_str, gdi.bitmapcoreinfo, tagBITMAPCOREINFO, wingdi/BITMAPCOREINFO, wingdi/PBITMAPCOREINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - BITMAPCOREINFO
product: Windows
targetos: Windows
req.typenames: BITMAPCOREINFO, *LPBITMAPCOREINFO, *PBITMAPCOREINFO
req.redist: 
---

# tagBITMAPCOREINFO structure


## -description



The <b>BITMAPCOREINFO</b> structure defines the dimensions and color information for a DIB.




## -struct-fields




### -field bmciHeader

A <a href="https://msdn.microsoft.com/0182adcd-dbba-43de-b41b-ab2f0fd8f7bf">BITMAPCOREHEADER</a> structure that contains information about the dimensions and color format of a DIB.


### -field bmciColors

Specifies an array of <a href="https://msdn.microsoft.com/bc1467a5-0027-4f22-bfc9-1deab562c573">RGBTRIPLE</a> structures that define the colors in the bitmap.


## -remarks



A DIB consists of two parts: a <b>BITMAPCOREINFO</b> structure describing the dimensions and colors of the bitmap, and an array of bytes defining the pixels of the bitmap. The bits in the array are packed together, but each scan line must be padded with zeros to end on a <b>LONG</b> boundary. The origin of the bitmap is the lower-left corner.

The <b>bcBitCount</b> member of the <a href="https://msdn.microsoft.com/0182adcd-dbba-43de-b41b-ab2f0fd8f7bf">BITMAPCOREHEADER</a> structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>1</td>
<td>The bitmap is monochrome, and the <b>bmciColors</b> member contains two entries. Each bit in the bitmap array represents a pixel. If the bit is clear, the pixel is displayed with the color of the first entry in the <b>bmciColors</b> table; if the bit is set, the pixel has the color of the second entry in the table.</td>
</tr>
<tr>
<td>4</td>
<td>The bitmap has a maximum of 16 colors, and the <b>bmciColors</b> member contains up to 16 entries. Each pixel in the bitmap is represented by a 4-bit index into the color table. For example, if the first byte in the bitmap is 0x1F, the byte represents two pixels. The first pixel contains the color in the second table entry, and the second pixel contains the color in the sixteenth table entry.</td>
</tr>
<tr>
<td>8</td>
<td>The bitmap has a maximum of 256 colors, and the <b>bmciColors</b> member contains up to 256 entries. In this case, each byte in the array represents a single pixel.</td>
</tr>
<tr>
<td>24</td>
<td>The bitmap has a maximum of 2 (24) colors, and the <b>bmciColors</b> member is <b>NULL</b>. Each three-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</td>
</tr>
</table>
 

The colors in the <b>bmciColors</b> table should appear in order of importance.

Alternatively, for functions that use DIBs, the <b>bmciColors</b> member can be an array of 16-bit unsigned integers that specify indexes into the currently realized logical palette, instead of explicit RGB values. In this case, an application using the bitmap must call the DIB functions ( <a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>, <a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>, and <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a> ) with the <i>iUsage</i> parameter set to DIB_PAL_COLORS.

<div class="alert"><b>Note</b>  <p class="note">The <b>bmciColors</b> member should not contain palette indexes if the bitmap is to be stored in a file or transferred to another application. Unless the application has exclusive use and control of the bitmap, the bitmap color table should contain explicit RGB values.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0182adcd-dbba-43de-b41b-ab2f0fd8f7bf">BITMAPCOREHEADER</a>



<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>



<a href="https://msdn.microsoft.com/bc1467a5-0027-4f22-bfc9-1deab562c573">RGBTRIPLE</a>
 

 

