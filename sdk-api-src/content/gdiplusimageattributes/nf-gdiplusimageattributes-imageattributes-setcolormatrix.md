---
UID: NF:gdiplusimageattributes.ImageAttributes.SetColorMatrix
title: ImageAttributes::SetColorMatrix
author: windows-sdk-content
description: The ImageAttributes::SetColorMatrix method sets the color-adjustment matrix for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetColorMatrix_colorMatrix_mode_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setcolormatrix.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ImageAttributes class [GDI+],SetColorMatrix method, ImageAttributes.SetColorMatrix, ImageAttributes::SetColorMatrix, SetColorMatrix, SetColorMatrix method [GDI+], SetColorMatrix method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetColorMatrix_colorMatrix_mode_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetColorMatrix_colorMatrix_mode_type_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusimageattributes.h
req.include-header: Gdiplus.h
req.redist: 
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
 - ImageAttributes.SetColorMatrix
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetColorMatrix


## -description


The <b>ImageAttributes::SetColorMatrix</b> method sets the color-adjustment matrix for a specified category.


## -parameters




### -param colorMatrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a>*</b>

Pointer to a 5×5 color-adjustment matrix. 


### -param mode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534091(v=VS.85).aspx">ColorMatrixFlags</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534091(v=VS.85).aspx">ColorMatrixFlags</a> enumeration that specifies the type of image and color that will be affected by the color-adjustment matrix. 


### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the color-adjustment matrix is set. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



An <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color-adjustment matrix for the default category, a different color-adjustment matrix for the bitmap category, and still a different color-adjustment matrix for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the color-adjustment matrix for the pen category by passing <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetColorMatrix</b> method, then none of the default adjustment settings will apply to pens.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535416(v=VS.85).aspx">ImageAttributes::ClearColorMatrices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535417(v=VS.85).aspx">ImageAttributes::ClearColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535430(v=VS.85).aspx">ImageAttributes::SetColorMatrices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535438(v=VS.85).aspx">ImageAttributes::SetToIdentity</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

