---
UID: NF:gdiplusheaders.Image.SetPalette
title: Image::SetPalette
author: windows-driver-content
description: The Image::SetPalette method sets the color palette of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_SetPalette_palette_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\setpalette.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Image.SetPalette
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Image::SetPalette


## -description


The <b>Image::SetPalette</b> method sets the color palette of this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


## -parameters




### -param palette [in]

Type: <b>const ColorPalette*</b>

Pointer to a <a href="https://msdn.microsoft.com/10b81e2d-00a2-4f36-bd9d-3dddb68de781">ColorPalette</a> structure that specifies the palette. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/10b81e2d-00a2-4f36-bd9d-3dddb68de781">ColorPalette</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ffe250ce-0ebc-4470-846f-f45a1de5165e">Image::GetPalette</a>



<a href="https://msdn.microsoft.com/f9721828-65b6-4cee-b418-a54b6f9d32ed">Image::GetPaletteSize</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

