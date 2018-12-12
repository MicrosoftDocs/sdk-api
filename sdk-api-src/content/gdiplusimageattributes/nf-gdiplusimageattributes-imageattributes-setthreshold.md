---
UID: NF:gdiplusimageattributes.ImageAttributes.SetThreshold
title: ImageAttributes::SetThreshold
author: windows-sdk-content
description: The ImageAttributes::SetThreshold method sets the threshold (transparency range) for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetThreshold_threshold_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setthreshold.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImageAttributes class [GDI+],SetThreshold method, ImageAttributes.SetThreshold, ImageAttributes::SetThreshold, SetThreshold, SetThreshold method [GDI+], SetThreshold method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetThreshold_threshold_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetThreshold_threshold_type_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ImageAttributes.SetThreshold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetThreshold


## -description


The <b>ImageAttributes::SetThreshold</b> method sets the threshold (transparency range) for a specified category.


## -parameters




### -param threshold [in]

Type: <b>REAL</b>

<b>REAL</b> number that specifies the threshold value. 


### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a> enumeration that specifies the category for which the color threshold is set. The default value is <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The threshold is a value from 0 through 1 that specifies a cutoff point for each color component. For example, suppose the threshold is set to 0.7, and suppose you are rendering a color whose red, green, and blue components are 230, 50, and 220. The red component, 230, is greater than 0.7×255, so the red component will be changed to 255 (full intensity). The green component, 50, is less than 0.7×255, so the green component will be changed to 0. The blue component, 220, is greater than 0.7×255, so the blue component will be changed to 255.

An <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a threshold for the default category, a threshold for the bitmap category, and still a different threshold for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the threshold for the pen category by passing <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetThreshold</b> method, then none of the default adjustment settings will apply to pens.


#### Examples



The following example creates an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object based on a .bmp file. The code also creates an <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object and sets its bitmap threshold value to 0.6. Then the code draws the image twice: once with no color adjustment and once with the adjustment specified by the threshold.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID Example_SetThreshold(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an Image object based on a .bmp file.
   // The image has one stripe with RGB components (160, 0, 0)
   // and one stripe with RGB components (0, 140, 0).
   Image image(L"RedGreenThreshold.bmp");

   // Create an ImageAttributes object, and set its bitmap threshold to 0.6.
   ImageAttributes imAtt;
   imAtt.SetThreshold(0.6f, ColorAdjustTypeBitmap);

   // Draw the image with no color adjustment.
   graphics.DrawImage(&amp;image, 10, 10, image.GetWidth(), image.GetHeight());
 
   // Draw the image with the threshold applied.
   // 160 &gt; 0.6*255, so the red stripe will be changed to full intensity.
   // 140 &lt; 0.6*255, so the green stripe will be changed to zero intensity.   
   graphics.DrawImage(&amp;image,
      Rect(100, 10, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),           // source rect
      UnitPixel,
      &amp;imAtt);
}
				</pre>
</td>
</tr>
</table></span></div>
The following illustration shows the output of the preceding code. Note that the red was converted to maximum intensity, and the green was converted to zero intensity.

<img alt="Illustration showing a rectangle with maroon and green regions, then the same rectangle but rendered in red and black" src="./images/imageattributessetthreshold.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/3bf053e5-bd05-40fb-986c-67e6dce0b72a">ImageAttributes::ClearColorKey</a>



<a href="https://msdn.microsoft.com/beaaab07-0ebe-4c29-b49b-2d998c782ce6">ImageAttributes::ClearThreshold</a>



<a href="https://msdn.microsoft.com/d58ba121-877a-447b-8920-440ab3686d7e">ImageAttributes::SetColorKey</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>
 

 

