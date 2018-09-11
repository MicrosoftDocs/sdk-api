---
UID: NF:gdiplusheaders.Image.SetPalette
title: Image::SetPalette
author: windows-sdk-content
description: The Image::SetPalette method sets the color palette of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_SetPalette_palette_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\setpalette.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Image class [GDI+],SetPalette method, Image.SetPalette, Image::SetPalette, SetPalette, SetPalette method [GDI+], SetPalette method [GDI+],Image class, _gdiplus_CLASS_Image_SetPalette_palette_, gdiplus._gdiplus_CLASS_Image_SetPalette_palette_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - Image.SetPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::SetPalette


## -description


The <b>Image::SetPalette</b> method sets the color palette of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object.


## -parameters




### -param palette [in]

Type: <b>const ColorPalette*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a> structure that specifies the palette. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535384(v=VS.85).aspx">Image::GetPalette</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535385(v=VS.85).aspx">Image::GetPaletteSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536335(v=VS.85).aspx">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533815(v=VS.85).aspx">Using Images, Bitmaps, and Metafiles</a>
 

 

