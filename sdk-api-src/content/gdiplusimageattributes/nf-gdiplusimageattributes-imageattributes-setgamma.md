---
UID: NF:gdiplusimageattributes.ImageAttributes.SetGamma
title: ImageAttributes::SetGamma
author: windows-sdk-content
description: The ImageAttributes::SetGamma method sets the gamma value for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetGamma_gamma_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setgamma.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ImageAttributes class [GDI+],SetGamma method, ImageAttributes.SetGamma, ImageAttributes::SetGamma, SetGamma, SetGamma method [GDI+], SetGamma method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetGamma_gamma_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetGamma_gamma_type_
ms.prod: windows
ms.technology: windows-sdk
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
 - ImageAttributes.SetGamma
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetGamma


## -description


The <b>ImageAttributes::SetGamma</b> method sets the gamma value for a specified category.


## -parameters




### -param gamma [in]

Type: <b>REAL</b>

<b>REAL</b> number that specifies the gamma value. 


### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the gamma value is set. The default value is <a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



An 
				<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a gamma value for the default category, a different gamma value for the bitmap category, and still a different gamma value for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the gamma value for the pen category by passing <a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetGamma</b> method, then none of the default adjustment settings will apply to pens.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/library/ms535418(v=VS.85).aspx">ImageAttributes::ClearGamma</a>



<a href="https://msdn.microsoft.com/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

