---
UID: NF:gdiplusgraphics.Graphics.FromImage
title: Graphics::FromImage
author: windows-sdk-content
description: The Graphics::FromImage method creates a Graphicsobject that is associated with a specified Image object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FromImage_image_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\fromimage.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: FromImage, FromImage method [GDI+], FromImage method [GDI+],Graphics class, Graphics class [GDI+],FromImage method, Graphics.FromImage, Graphics::FromImage, _gdiplus_CLASS_Graphics_FromImage_image_, gdiplus._gdiplus_CLASS_Graphics_FromImage_image_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Graphics.FromImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::FromImage


## -description


The <b>Graphics::FromImage</b> method creates a 
			<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>object that is associated with a specified 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an 
					<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that will be associated with the new 
					<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>object.




## -remarks



This method fails if the 
				<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object is based on a metafile that was opened for reading. The 
				<a href="https://msdn.microsoft.com/35c4b98b-6fbb-4506-9437-756d0d90ce8a">Image::Image(filename, useEmbeddedColorManagement)</a> and 
				<a href="https://msdn.microsoft.com/1bccba1d-63e4-469d-a7b8-0f83ff7ebcc0">Metafile::Metafile(filename)</a> constructors open a metafile for reading. To open a metafile for recording, use a 
				<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> constructor that receives a device context handle.

This method also fails if the image has one of the following pixel formats: 

<ul>
<li><b>PixelFormatUndefined</b></li>
<li><b>PixelFormatDontCare</b></li>
<li><b>PixelFormat1bppIndexed</b></li>
<li><b>PixelFormat4bppIndexed</b></li>
<li><b>PixelFormat8bppIndexed</b></li>
<li><b>PixelFormat16bppGrayScale</b></li>
<li><b>PixelFormat16bppARGB1555</b></li>
</ul>

#### Examples



The following example calls the <b>Graphics::FromImage</b> method to create a 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>object that is associated with an 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object. The call to 
						<a href="https://msdn.microsoft.com/580a46f7-c2ad-40fe-b87c-08a6648a9df6">Graphics::FillEllipse</a>	does not paint on the display device; instead, it alters the bitmap of the 
						<b>Image</b> object. The call to 
						<a href="https://msdn.microsoft.com/7864f9f6-40c0-428c-8867-2a37abed0505">Graphics::DrawImage</a> displays the altered bitmap.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_FromImage(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an Image object from a PNG file.
   Image image(L"Mosaic.png");

   // Create a Graphics object that is associated with the image.
   Graphics* imageGraphics = Graphics::FromImage(&amp;image);
   
   // Alter the image.
   SolidBrush brush(Color(255, 0, 0, 255));
   imageGraphics-&gt;FillEllipse(&amp;brush, 10, 40, 100, 50);

   // Draw the altered image.
   graphics.DrawImage(&amp;image, 30, 20);
   
   delete imageGraphics;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/89a154c1-6a49-45d6-a73c-94b0b1567408">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/c1d3fc6e-6b7d-4fcf-9bc4-a2bab36304ed">FromHDC Methods</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/76c4c444-cd6f-43ff-8ab7-96469d4505b9">Graphics Constructors</a>



<a href="https://msdn.microsoft.com/e7c9c984-01cd-45de-95da-378df13f570b">Graphics::FromHWND</a>



<a href="https://msdn.microsoft.com/b1a81c8b-7968-4ad8-a7b6-ebe6c266fd0b">Graphics::GetHDC</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

