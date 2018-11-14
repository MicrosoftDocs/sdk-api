---
UID: NF:gdiplusimageattributes.ImageAttributes.SetColorMatrices
title: ImageAttributes::SetColorMatrices
author: windows-sdk-content
description: The ImageAttributes::SetColorMatrices method sets the color-adjustment matrix and the grayscale-adjustment matrix for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetColorMatrices_colorMatrix_grayMatrix_mode_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setcolormatrices.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ImageAttributes class [GDI+],SetColorMatrices method, ImageAttributes.SetColorMatrices, ImageAttributes::SetColorMatrices, SetColorMatrices, SetColorMatrices method [GDI+], SetColorMatrices method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetColorMatrices_colorMatrix_grayMatrix_mode_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetColorMatrices_colorMatrix_grayMatrix_mode_type_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusimageattributes.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
 - ImageAttributes.SetColorMatrices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusimageattributes.h
: 
- ImageAttributes.SetColorMatrices
: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetColorMatrices


## -description


The <b>ImageAttributes::SetColorMatrices</b> method sets the color-adjustment matrix and the grayscale-adjustment matrix for a specified category.


## -parameters




### -param colorMatrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a>*</b>

Pointer to a 5×5 color-adjustment matrix. 


### -param grayMatrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a>*</b>

Pointer to a 5×5 grayscale-adjustment matrix. 


### -param mode [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534091(v=VS.85).aspx">ColorMatrixFlags</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534091(v=VS.85).aspx">ColorMatrixFlags</a> enumeration that specifies the type of image and color that will be affected by the color-adjustment and grayscale-adjustment matrices. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534091(v=VS.85).aspx">ColorMatrixFlagsDefault</a>. 


### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the color-adjustment and grayscale-adjustment matrices are set. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



An 
				<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify adjustment matrices for the default category, different adjustment matrices for the bitmap category, and still different adjustment matrices for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the color-adjustment and grayscale-adjustment matrices for the pen category by passing <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetColorMatrices</b> method, then none of the default adjustment settings will apply to pens.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535416(v=VS.85).aspx">ImageAttributes::ClearColorMatrices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535417(v=VS.85).aspx">ImageAttributes::ClearColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535431(v=VS.85).aspx">ImageAttributes::SetColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535438(v=VS.85).aspx">ImageAttributes::SetToIdentity</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

