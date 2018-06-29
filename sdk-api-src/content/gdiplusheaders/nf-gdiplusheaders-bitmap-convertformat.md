---
UID: NF:gdiplusheaders.Bitmap.ConvertFormat
title: Bitmap::ConvertFormat
author: windows-sdk-content
description: The Bitmap::ConvertFormat method converts a bitmap to a specified pixel format. The original pixel data in the bitmap is replaced by the new pixel data.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_ConvertFormat_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapgethistogrammethods\convertformat.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Bitmap class [GDI+],ConvertFormat method, Bitmap.ConvertFormat, Bitmap::ConvertFormat, ConvertFormat, ConvertFormat method [GDI+], ConvertFormat method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_ConvertFormat_, gdiplus._gdiplus_CLASS_Bitmap_ConvertFormat_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.ConvertFormat
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# Bitmap::ConvertFormat


## -description


The <b>Bitmap::ConvertFormat</b> method converts a bitmap to a specified pixel format. The original pixel data in the bitmap is replaced by the new pixel data.


## -parameters




### -param format [in]

Type: <b>PixelFormat</b>


<a href="https://msdn.microsoft.com/library/ms534412(v=VS.85).aspx">Pixel format constant</a> that specifies the new pixel format.


### -param dithertype [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms534106(v=VS.85).aspx">DitherType</a></b>

Element of the <a href="https://msdn.microsoft.com/library/ms534106(v=VS.85).aspx">DitherType</a> enumeration that specifies the dithering algorithm. In cases where the conversion does not reduce the bit depth of the pixel data, pass <b>DitherTypeNone</b>.


### -param palettetype [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms534159(v=VS.85).aspx">PaletteType</a></b>

Element of the <a href="https://msdn.microsoft.com/library/ms534159(v=VS.85).aspx">PaletteType</a> enumeration that specifies a standard palette to be used for dithering. If you are converting to a non-indexed format, this parameter is ignored. In that case, pass any element of the <b>PaletteType</b> enumeration, say <b>PaletteTypeCustom</b>.


### -param palette [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms534064(v=VS.85).aspx">ColorPalette</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms534064(v=VS.85).aspx">ColorPalette</a> structure that specifies the palette whose indexes are stored in the pixel data of the converted bitmap. This palette (called the actual palette) does not have to have the type specified by the <i>palettetype</i> parameter. The <i>palettetype</i> parameter specifies a standard palette that can be used by any of the ordered or spiral dithering algorithms. If the actual palette has a type other than that specified by the <i>palettetype</i> parameter, then the <b>Bitmap::ConvertFormat</b> method performs a nearest-color conversion from the standard palette to the actual palette.


### -param alphaThresholdPercent [in]

Type: <b>REAL</b>

Real number in the range 0 through 100 that specifies which pixels in the source bitmap will map to the transparent color in the converted bitmap. A value of 0 specifies that none of the source pixels map to the transparent color. A value of 100 specifies that any pixel that is not fully opaque will map to the transparent color. A value of t specifies that any source pixel less than t percent of fully opaque will map to the transparent color. Note that for the alpha threshold to be effective, the palette must have a transparent color. If the palette does not have a transparent color, pixels with alpha values below the threshold will map to color that most closely matches (0, 0, 0, 0), usually black.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/library/ms536309(v=VS.85).aspx">Bitmap::InitializePalette</a>
 

 

