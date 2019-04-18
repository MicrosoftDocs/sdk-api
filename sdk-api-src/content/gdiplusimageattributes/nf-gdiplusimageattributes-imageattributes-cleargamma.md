---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearGamma
title: ImageAttributes::ClearGamma (gdiplusimageattributes.h)
author: windows-sdk-content
description: The ImageAttributes::ClearGamma method disables gamma correction for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearGamma_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\cleargamma.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClearGamma, ClearGamma method [GDI+], ClearGamma method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearGamma method, ImageAttributes.ClearGamma, ImageAttributes::ClearGamma, _gdiplus_CLASS_ImageAttributes_ClearGamma_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearGamma_type_
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
 - ImageAttributes.ClearGamma
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# ImageAttributes::ClearGamma


## -description


The <b>ImageAttributes::ClearGamma</b> method disables gamma correction for a specified category.


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which gamma correction is disabled. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



An 
				<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a gamma value for the default category, a different gamma value for the bitmap category, and still a different gamma value for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a gamma value and a color-adjustment matrix for the default category. If you set the gamma value for the pen category by calling <a href="https://msdn.microsoft.com/en-us/library/ms535432(v=VS.85).aspx">ImageAttributes::SetGamma</a>, then the default gamma value will not apply to pens. If you later clear the pen gamma value by calling <b>ImageAttributes::ClearGamma</b>, the pen category will not revert to the default gamma value; rather, the pen category will have no gamma value. Similarly, the pen category will not revert to the default color-adjustment matrix; rather, the pen category will have no color-adjustment matrix.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535432(v=VS.85).aspx">ImageAttributes::SetGamma</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

