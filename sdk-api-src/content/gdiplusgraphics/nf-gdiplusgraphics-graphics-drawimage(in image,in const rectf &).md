---
UID: NF:gdiplusgraphics.Graphics.DrawImage(IN Image,IN const RectF &)
title: Graphics::DrawImage(IN Image,IN const RectF &)
author: windows-sdk-content
description: The Graphics::DrawImage method draws an image.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_55imageimage_rectfamprect.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN const RectF &), Graphics.DrawImage(Image*,const RectF&), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN const RectF &), _gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_rect_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_rect_
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
 - Graphics.DrawImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawImage(IN Image,IN const RectF &)


## -description


The <b>Graphics::DrawImage</b> method draws an image.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that specifies the source image. 


### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a></b>

Reference to a rectangle that bounds the drawing area for the image. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The image is scaled to fit the rectangle.


#### Examples



The following example draws the source image, the rectangle that bounds the resized image, and then draws the resized image to fit the rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_DrawImage10(HDC hdc)

{
   Graphics graphics(hdc);

   // Create an Image object.
   Image image(L"climber.jpg");

   // Create a Pen object.
   Pen pen (Color(255, 255, 0, 0), 2);

   // Draw the original source image.
   graphics.DrawImage(&amp;image, 10, 10);

   // Create a RectF object that specifies the destination of the image.
   RectF destRect(200, 50, 150, 75);

   // Draw the rectangle that bounds the image.
   graphics.DrawRectangle(&amp;pen, destRect);

   // Draw the image.
   graphics.DrawImage(&amp;image, destRect);
}</pre>
</td>
</tr>
</table></span></div>
The following illustration shows the output of the preceding code.

<img alt="Illustration showing two versions of the same image; the second is slightly narrower than the first, much shorter, and outlined in red" src="images/drawimage6.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0ad2a132-6db6-4099-81a2-10e1cd1b1f61">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>
 

 

