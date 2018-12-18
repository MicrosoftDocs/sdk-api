---
UID: NF:gdiplusgraphics.Graphics.Graphics(IN Image)
title: Graphics::Graphics(IN Image)
author: windows-sdk-content
description: Creates a Graphics::Graphics object that is associated with an Image object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_Graphics_image_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsconstructors\graphics_30image.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Graphics, Graphics class [GDI+],Graphics constructor, Graphics constructor [GDI+], Graphics constructor [GDI+],Graphics class, Graphics.Graphics, Graphics.Graphics(IN Image), Graphics.Graphics(Image*), Graphics::Graphics, Graphics::Graphics(IN Image), _gdiplus_CLASS_Graphics_Graphics_image_, gdiplus._gdiplus_CLASS_Graphics_Graphics_image_
ms.topic: method
req.header: gdiplusgraphics.h
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
 - Graphics.Graphics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::Graphics(IN Image)


## -description


Creates a <b>Graphics::Graphics</b> object that is associated with an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


## -parameters




### -param image [in]

Type: <b>Image*</b>

Pointer to an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that will be associated with the new <b>Graphics::Graphics</b> object. 


## -remarks



This constructor fails if the <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object is based on a metafile that was opened for reading. The 
				<b>Image::Image(file)</b> and 
				<b>Metafile::Metafile(file)</b> constructors open a metafile for reading. To open a metafile for recording, use a 
				<b>Metafile</b> constructor that receives a device context handle.

This constructor also fails if the image uses one of the following pixel formats: 

<ul>
<li>PixelFormatUndefined </li>
<li>PixelFormatDontCare </li>
<li>PixelFormat1bppIndexed </li>
<li>PixelFormat4bppIndexed </li>
<li>PixelFormat8bppIndexed </li>
<li>PixelFormat16bppGrayScale </li>
<li>PixelFormat16bppARGB1555 </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/89a154c1-6a49-45d6-a73c-94b0b1567408">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/c03c5ef1-13f6-4cf5-9395-be90b46aa6bb">Getting Started</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/76c4c444-cd6f-43ff-8ab7-96469d4505b9">Graphics Constructors</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>
 

 

