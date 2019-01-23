---
UID: NF:gdiplusgraphics.Graphics.DrawImage(IN Image,IN const Point,IN INT)
title: Graphics::DrawImage(IN Image,IN const Point,IN INT)
author: windows-sdk-content
description: The Graphics::DrawImage method draws an image.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_Point_destPoints_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN const Point,IN INT), Graphics.DrawImage(Image*,const Point*,INT), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN const Point,IN INT), _gdiplus_CLASS_Graphics_DrawImage_Image_image_Point_destPoints_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_Point_destPoints_INT_count_
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

# Graphics::DrawImage(IN Image,IN const Point,IN INT)


## -description


The <b>Graphics::DrawImage</b> method draws an image.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object that specifies the source image. 


### -param destPoints [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a> objects that specify the area, in a parallelogram, in which to draw the image. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>destPoints</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns <b>InvalidParameter</b>.




## -remarks



The value of the 
				<i>count</i> parameter must equal 3 to specify the three corners of the parallelogram. The fourth corner of the parallelogram is calculated using the vectors of the first and second coordinates and the first and third coordinates. The image is scaled to fit the parallelogram.


#### Examples



The following example draws an image.


```cpp
VOID Example_DrawImage(HDC hdc)

{

   Graphics graphics(hdc);

   // Create an Image object.
   Image image(L"climber.jpg");

   // Create an array of Point objects that specify the destination of the image.
   Point destPoints[3] = {
   Point(30, 30),
   Point(250, 50),
   Point(175, 120)};

   Point* pdestPoints = destPoints;

   // Draw the image.
   graphics.DrawImage(&image, pdestPoints, 3);
}
```


The following illustration shows the output of the preceding code.

<img alt="Illustration showing a previously-rectangular image that is now sheared to a parallelogram" src="images/drawimage1.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536388(v=VS.85).aspx">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533830(v=VS.85).aspx">Loading and Displaying Bitmaps</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>
 

 

