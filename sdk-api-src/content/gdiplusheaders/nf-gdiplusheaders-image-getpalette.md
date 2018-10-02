---
UID: NF:gdiplusheaders.Image.GetPalette
title: Image::GetPalette
author: windows-sdk-content
description: The Image::GetPalette method gets the ColorPalette of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetPalette_palette_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getpalette.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPalette, GetPalette method [GDI+], GetPalette method [GDI+],Image class, Image class [GDI+],GetPalette method, Image.GetPalette, Image::GetPalette, _gdiplus_CLASS_Image_GetPalette_palette_size_, gdiplus._gdiplus_CLASS_Image_GetPalette_palette_size_
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
 - Image.GetPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::GetPalette


## -description


The <b>Image::GetPalette</b> method gets the <a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a> of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object. 


## -parameters




### -param palette [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a> structure that receives the palette. 


### -param size [in]

Type: <b>INT</b>

Integer that specifies the size, in bytes, of the palette. Call the <a href="https://msdn.microsoft.com/en-us/library/ms535385(v=VS.85).aspx">Image::GetPaletteSize</a> method to determine the size. 


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



<a href="https://msdn.microsoft.com/en-us/library/ms535385(v=VS.85).aspx">Image::GetPaletteSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535404(v=VS.85).aspx">Image::SetPalette</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536335(v=VS.85).aspx">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533815(v=VS.85).aspx">Using Images, Bitmaps, and Metafiles</a>
 

 

