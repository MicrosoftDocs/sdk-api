---
UID: NS:wingdi.tagBITMAPINFO
title: BITMAPINFO (wingdi.h)
description: The BITMAPINFO structure defines the dimensions and color information for a DIB.
helpviewer_keywords: ["*LPBITMAPINFO","*PBITMAPINFO","BITMAPINFO","BITMAPINFO structure [Windows GDI]","PBITMAPINFO","PBITMAPINFO structure pointer [Windows GDI]","_win32_BITMAPINFO_str","gdi.bitmapinfo","tagBITMAPINFO","wingdi/BITMAPINFO","wingdi/PBITMAPINFO"]
old-location: gdi\bitmapinfo.htm
tech.root: gdi
ms.assetid: 84cc51e8-78f3-4ee6-bc08-94feff89afb0
ms.date: 12/05/2018
ms.keywords: '*LPBITMAPINFO, *PBITMAPINFO, BITMAPINFO, BITMAPINFO structure [Windows GDI], PBITMAPINFO, PBITMAPINFO structure pointer [Windows GDI], _win32_BITMAPINFO_str, gdi.bitmapinfo, tagBITMAPINFO, wingdi/BITMAPINFO, wingdi/PBITMAPINFO'
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
targetos: Windows
req.typenames: BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagBITMAPINFO
 - wingdi/tagBITMAPINFO
 - LPBITMAPINFO
 - wingdi/LPBITMAPINFO
 - BITMAPINFO
 - wingdi/BITMAPINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - BITMAPINFO
---

# BITMAPINFO structure


## -description

The <b>BITMAPINFO</b> structure defines the dimensions and color information for a DIB.

## -struct-fields

### -field bmiHeader

A <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure that contains information about the dimensions of color format.

.

### -field bmiColors

The <b>bmiColors</b> member contains one of the following:

<ul>
<li>An array of <a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>. The elements of the array that make up the color table.</li>
<li>An array of 16-bit unsigned integers that specifies indexes into the currently realized logical palette. This use of <b>bmiColors</b> is allowed for functions that use DIBs. When <b>bmiColors</b> elements contain indexes to a realized logical palette, they must also call the following bitmap functions:



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>


The <i>iUsage</i> parameter of <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a> must be set to DIB_PAL_COLORS.

</li>
</ul>
The number of entries in the array depends on the values of the <b>biBitCount</b> and <b>biClrUsed</b> members of the <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

The colors in the <b>bmiColors</b> table appear in order of importance. For more information, see the Remarks section.

## -remarks

A DIB consists of two distinct parts: a <b>BITMAPINFO</b> structure describing the dimensions and colors of the bitmap, and an array of bytes defining the pixels of the bitmap. The bits in the array are packed together, but each scan line must be padded with zeros to end on a <b>LONG</b> data-type boundary. If the height of the bitmap is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner. If the height is negative, the bitmap is a top-down DIB and its origin is the upper left corner.

A bitmap is packed when the bitmap array immediately follows the <b>BITMAPINFO</b> header. Packed bitmaps are referenced by a single pointer. For packed bitmaps, the <b>biClrUsed</b> member must be set to an even number when using the DIB_PAL_COLORS mode so that the DIB bitmap array starts on a <b>DWORD</b> boundary.

<div class="alert"><b>Note</b>  <p class="note">The <b>bmiColors</b> member should not contain palette indexes if the bitmap is to be stored in a file or transferred to another application.

<p class="note">Unless the application has exclusive use and control of the bitmap, the bitmap color table should contain explicit RGB values.

</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a>



<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>
