---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearColorKey
title: ImageAttributes::ClearColorKey
author: windows-sdk-content
description: The ImageAttributes::ClearColorKey method clears the color key (transparency range) for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearColorKey_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearcolorkey.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ClearColorKey, ClearColorKey method [GDI+], ClearColorKey method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearColorKey method, ImageAttributes.ClearColorKey, ImageAttributes::ClearColorKey, _gdiplus_CLASS_ImageAttributes_ClearColorKey_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearColorKey_type_
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	ImageAttributes.ClearColorKey
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::ClearColorKey


## -description


The <b>ImageAttributes::ClearColorKey</b> method clears the color key (transparency range) for a specified category.


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a> enumeration that specifies the category for which the color key is cleared. The default value is <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



An <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify one color key for the default category, a different color key for the bitmap category, and still a different color key for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a default color key that makes any color with a red component from 200 through 255 transparent and you specify a default gamma value of 1.8. If you set the color key of the pen category by calling <a href="https://msdn.microsoft.com/d58ba121-877a-447b-8920-440ab3686d7e">ImageAttributes::SetColorKey</a>, then the default color key and the default gamma value will not apply to pens. If you later clear the pen color key by calling <b>ImageAttributes::ClearColorKey</b>, the pen category will not revert to the default color key; rather, the pen category will have no color key. Similarly, the pen category will not revert to the default gamma value; rather, the pen category will have no gamma value.


#### Examples



The following example creates an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object from a .emf file. The code also creates an <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object. The first call to <a href="https://msdn.microsoft.com/d58ba121-877a-447b-8920-440ab3686d7e">ImageAttributes::SetColorKey</a> sets the default color key of the 
<b>ImageAttributes</b> object so that colors with a red component from 80 through 120 are transparent. The second call to <b>ImageAttributes::SetColorKey</b> sets the pen color key of the <b>ImageAttributes</b> object so that all colors with a red component from 135 through 175 are transparent.

The code calls <a href="https://msdn.microsoft.com/d604d511-c8d7-4e3b-8d54-be06823dbd1f">DrawImage</a> once to draw the image with no color adjustment. Then the code calls <b>DrawImage</b> three more times, each time passing the address of the <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object and the address of the <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object. The second time the image is drawn (after the call that sets the default color key), all of the red from 80 through 120 is transparent. The third time the image is drawn (after the call that sets the pen color key), all of the red from 135 through 175 that is drawn with a pen is transparent. Also, all of the red from 80 through 120 that is not drawn with a pen is transparent. The fourth time the image is drawn (after the call to <b>ImageAttributes::ClearColorKey</b>), none of the red drawn with a pen is transparent. Also, all of the red from 80 through 120 that is not drawn with a pen is transparent.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID Example_SetClearColorKey(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"TestMetafile5.emf");
   ImageAttributes imAtt;

   // Draw the image (metafile) using no color adjustment.
   graphics.DrawImage(
      &amp;image,
      Rect(0, 0, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),        // source rect
      UnitPixel);

   // Set the default color key.
   imAtt.SetColorKey(
      Color(0, 80, 0, 0),
      Color(255, 120, 255, 255),
      ColorAdjustTypeDefault);

   // Draw the image (metafile) using default color adjustment.
   // Colors with red components from 80 through 120 are transparent.
   graphics.DrawImage(
      &amp;image,
      Rect(0, 100, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &amp;imAtt);

   // Set the pen color key.
   imAtt.SetColorKey(
      Color(0, 135, 0, 0),
      Color(255, 175, 255, 255),
      ColorAdjustTypePen);

   // Draw the image (metafile) using default and pen adjustment.
   // Colors drawn with a pen that have red components from 135 through 175
   // are transparent. Colors not drawn with a pen that have red components
   // from 80 to 120 are transparent.
   graphics.DrawImage(
      &amp;image,
      Rect(0, 200, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &amp;imAtt);

   // Clear the pen color key.
   imAtt.ClearColorKey(ColorAdjustTypePen);

   // Draw the image (metafile) using only default color adjustment.
   // No colors drawn with a pen are transparent. Colors not drawn with 
   // a pen that have red components from 80 to 120 are transparent.
   graphics.DrawImage(
      &amp;image,
      Rect(0, 300, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &amp;imAtt); 
}
				</pre>
</td>
</tr>
</table></span></div>
The preceding code, along with a particular file, TestMetafile5.png, produced the following output. The bars in the left column were drawn with a pen, and the bars in the right column were filled with a brush. The default color key applies to the bars filled with a brush. The color key that applies to the bars drawn with a pen varies according to the <a href="https://msdn.microsoft.com/d58ba121-877a-447b-8920-440ab3686d7e">ImageAttributes::SetColorKey</a> and <b>ImageAttributes::ClearColorKey</b> calls.

<img alt="Illustration showing bars in four rows of two columns each; the last two have unequal numbers of bars in each row" src="images/imageattributesclearcolorkey.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/beaaab07-0ebe-4c29-b49b-2d998c782ce6">ImageAttributes::ClearThreshold</a>



<a href="https://msdn.microsoft.com/d58ba121-877a-447b-8920-440ab3686d7e">ImageAttributes::SetColorKey</a>



<a href="https://msdn.microsoft.com/25d57511-d81a-4fef-81b7-eed2501a74da">ImageAttributes::SetThreshold</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>
 

 

