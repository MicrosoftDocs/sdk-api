---
UID: NS:wingdi.tagBITMAPINFO
title: tagBITMAPINFO
author: windows-sdk-content
description: The BITMAPINFO structure defines the dimensions and color information for a DIB.
old-location: gdi\bitmapinfo.htm
old-project: gdi
ms.assetid: 84cc51e8-78f3-4ee6-bc08-94feff89afb0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*LPBITMAPINFO, *PBITMAPINFO, BITMAPINFO, BITMAPINFO structure [Windows GDI], PBITMAPINFO, PBITMAPINFO structure pointer [Windows GDI], _win32_BITMAPINFO_str, gdi.bitmapinfo, tagBITMAPINFO, wingdi/BITMAPINFO, wingdi/PBITMAPINFO"
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
tech.root: 
req.typenames: BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - BITMAPINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagBITMAPINFO structure


## -description



The <b>BITMAPINFO</b> structure defines the dimensions and color information for a DIB.




## -struct-fields




### -field bmiHeader

A <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure that contains information about the dimensions of color format.

.


### -field bmiColors

The <b>bmiColors</b> member contains one of the following:

<ul>
<li>An array of <a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD</a>. The elements of the array that make up the color table.</li>
<li>An array of 16-bit unsigned integers that specifies indexes into the currently realized logical palette. This use of <b>bmiColors</b> is allowed for functions that use DIBs. When <b>bmiColors</b> elements contain indexes to a realized logical palette, they must also call the following bitmap functions:
<a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>



<a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>


The <i>iUsage</i> parameter of <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a> must be set to DIB_PAL_COLORS.

</li>
</ul>
The number of entries in the array depends on the values of the <b>biBitCount</b> and <b>biClrUsed</b> members of the <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure.

The colors in the <b>bmiColors</b> table appear in order of importance. For more information, see the Remarks section.


## -remarks



A DIB consists of two distinct parts: a <b>BITMAPINFO</b> structure describing the dimensions and colors of the bitmap, and an array of bytes defining the pixels of the bitmap. The bits in the array are packed together, but each scan line must be padded with zeros to end on a <b>LONG</b> data-type boundary. If the height of the bitmap is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner. If the height is negative, the bitmap is a top-down DIB and its origin is the upper left corner.

A bitmap is packed when the bitmap array immediately follows the <b>BITMAPINFO</b> header. Packed bitmaps are referenced by a single pointer. For packed bitmaps, the <b>biClrUsed</b> member must be set to an even number when using the DIB_PAL_COLORS mode so that the DIB bitmap array starts on a <b>DWORD</b> boundary.

<div class="alert"><b>Note</b>  <p class="note">The <b>bmiColors</b> member should not contain palette indexes if the bitmap is to be stored in a file or transferred to another application.

<p class="note">Unless the application has exclusive use and control of the bitmap, the bitmap color table should contain explicit RGB values.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a>



<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>



<a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD</a>
 

 

