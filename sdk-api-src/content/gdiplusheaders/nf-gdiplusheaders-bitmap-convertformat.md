---
UID: NF:gdiplusheaders.Bitmap.ConvertFormat
title: Bitmap::ConvertFormat
author: windows-sdk-content
description: The Bitmap::ConvertFormat method converts a bitmap to a specified pixel format. The original pixel data in the bitmap is replaced by the new pixel data.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_ConvertFormat_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapgethistogrammethods\convertformat.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Bitmap class [GDI+],ConvertFormat method, Bitmap.ConvertFormat, Bitmap::ConvertFormat, ConvertFormat, ConvertFormat method [GDI+], ConvertFormat method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_ConvertFormat_, gdiplus._gdiplus_CLASS_Bitmap_ConvertFormat_
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
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
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Bitmap::ConvertFormat


## -description


The <b>Bitmap::ConvertFormat</b> method converts a bitmap to a specified pixel format. The original pixel data in the bitmap is replaced by the new pixel data.


## -parameters




### -param format [in]

Type: <b>PixelFormat</b>


<a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">Pixel format constant</a> that specifies the new pixel format.


### -param dithertype [in]

Type: <b><a href="https://msdn.microsoft.com/12fd01ec-948f-4e44-9947-4e08b29e53f7">DitherType</a></b>

Element of the <a href="https://msdn.microsoft.com/12fd01ec-948f-4e44-9947-4e08b29e53f7">DitherType</a> enumeration that specifies the dithering algorithm. In cases where the conversion does not reduce the bit depth of the pixel data, pass <b>DitherTypeNone</b>.


### -param palettetype [in]

Type: <b><a href="https://msdn.microsoft.com/8ab8678e-3a48-4747-8f1e-4c7fad370001">PaletteType</a></b>

Element of the <a href="https://msdn.microsoft.com/8ab8678e-3a48-4747-8f1e-4c7fad370001">PaletteType</a> enumeration that specifies a standard palette to be used for dithering. If you are converting to a non-indexed format, this parameter is ignored. In that case, pass any element of the <b>PaletteType</b> enumeration, say <b>PaletteTypeCustom</b>.


### -param palette [in]

Type: <b><a href="https://msdn.microsoft.com/10b81e2d-00a2-4f36-bd9d-3dddb68de781">ColorPalette</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/10b81e2d-00a2-4f36-bd9d-3dddb68de781">ColorPalette</a> structure that specifies the palette whose indexes are stored in the pixel data of the converted bitmap. This palette (called the actual palette) does not have to have the type specified by the <i>palettetype</i> parameter. The <i>palettetype</i> parameter specifies a standard palette that can be used by any of the ordered or spiral dithering algorithms. If the actual palette has a type other than that specified by the <i>palettetype</i> parameter, then the <b>Bitmap::ConvertFormat</b> method performs a nearest-color conversion from the standard palette to the actual palette.


### -param alphaThresholdPercent [in]

Type: <b>REAL</b>

Real number in the range 0 through 100 that specifies which pixels in the source bitmap will map to the transparent color in the converted bitmap. A value of 0 specifies that none of the source pixels map to the transparent color. A value of 100 specifies that any pixel that is not fully opaque will map to the transparent color. A value of t specifies that any source pixel less than t percent of fully opaque will map to the transparent color. Note that for the alpha threshold to be effective, the palette must have a transparent color. If the palette does not have a transparent color, pixels with alpha values below the threshold will map to color that most closely matches (0, 0, 0, 0), usually black.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/8a692b2b-e9b1-465e-9bfa-7306cd1d7ced">Bitmap::InitializePalette</a>
 

 

