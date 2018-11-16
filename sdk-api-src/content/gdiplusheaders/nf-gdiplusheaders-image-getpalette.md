---
UID: NF:gdiplusheaders.Image.GetPalette
title: Image::GetPalette
author: windows-sdk-content
description: The Image::GetPalette method gets the ColorPalette of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetPalette_palette_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getpalette.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
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
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Image.GetPalette
: 
req.product: GDI+ 1.0
---

# Image::GetPalette


## -description


The <b>Image::GetPalette</b> method gets the <a href="https://msdn.microsoft.com/10b81e2d-00a2-4f36-bd9d-3dddb68de781">ColorPalette</a> of this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object. 


## -parameters




### -param palette [out]

Type: <b><a href="https://msdn.microsoft.com/10b81e2d-00a2-4f36-bd9d-3dddb68de781">ColorPalette</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/10b81e2d-00a2-4f36-bd9d-3dddb68de781">ColorPalette</a> structure that receives the palette. 


### -param size [in]

Type: <b>INT</b>

Integer that specifies the size, in bytes, of the palette. Call the <a href="https://msdn.microsoft.com/f9721828-65b6-4cee-b418-a54b6f9d32ed">Image::GetPaletteSize</a> method to determine the size. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/10b81e2d-00a2-4f36-bd9d-3dddb68de781">ColorPalette</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/f9721828-65b6-4cee-b418-a54b6f9d32ed">Image::GetPaletteSize</a>



<a href="https://msdn.microsoft.com/62f1c8c0-788b-41e6-91af-15019b65bc3d">Image::SetPalette</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

