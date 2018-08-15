---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearBrushRemapTable
title: ImageAttributes::ClearBrushRemapTable
author: windows-sdk-content
description: The ImageAttributes::ClearBrushRemapTable method clears the brush color-remap table of this ImageAttributes object.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearBrushRemapTable_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearbrushremaptable.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ClearBrushRemapTable, ClearBrushRemapTable method [GDI+], ClearBrushRemapTable method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearBrushRemapTable method, ImageAttributes.ClearBrushRemapTable, ImageAttributes::ClearBrushRemapTable, _gdiplus_CLASS_ImageAttributes_ClearBrushRemapTable_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearBrushRemapTable_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusimageattributes.h
req.include-header: Gdiplus.h
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ImageAttributes.ClearBrushRemapTable
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::ClearBrushRemapTable


## -description


The <b>ImageAttributes::ClearBrushRemapTable</b> method clears the brush color-remap table of this <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



An <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify one color-remap table for the default category, a different color-remap table for the bitmap category, and still a different color-remap table for the brush category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the brush category, then the default settings apply to the brush category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a default remap table that converts red to green and you specify a default gamma value of 1.8. If you call <a href="https://msdn.microsoft.com/en-us/library/ms535428(v=VS.85).aspx">ImageAttributes::SetBrushRemapTable</a>, then the default remap table (red to green) and the default gamma value (1.8) will not apply to brushes. If you later call <b>ImageAttributes::ClearBrushRemapTable</b>, the brush category will not revert to the default remap table; rather, the brush category will have no remap table. Similarly, the brush category will not revert to the default gamma value; rather, the brush category will have no gamma value.


#### Examples



The following example creates an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object from a .emf file. The code also creates an <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. The call to <a href="https://msdn.microsoft.com/en-us/library/ms535436(v=VS.85).aspx">ImageAttributes::SetRemapTable</a> sets the default color-remap table of the <b>ImageAttributes</b> object to a table that converts red to blue. The call to <a href="https://msdn.microsoft.com/en-us/library/ms535428(v=VS.85).aspx">ImageAttributes::SetBrushRemapTable</a> sets the brush remap table of the <b>ImageAttributes</b> object to a table that converts red to green.

The code calls <a href="https://msdn.microsoft.com/en-us/library/ms536045(v=VS.85).aspx">DrawImage</a> once to draw the image with no color adjustment. Then the code calls <b>DrawImage</b> three more times, each time passing the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object and the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. The second time the image is drawn (after the call to <a href="https://msdn.microsoft.com/en-us/library/ms535436(v=VS.85).aspx">ImageAttributes::SetRemapTable</a>), all of the red is converted to blue. The third time the image is drawn (after the call to <a href="https://msdn.microsoft.com/en-us/library/ms535428(v=VS.85).aspx">ImageAttributes::SetBrushRemapTable</a>), all of the red painted with a brush is converted to green, and the rest of the red is converted to blue. The fourth time the image is drawn (after the call to <b>ImageAttributes::ClearBrushRemapTable</b>), all the red painted with a brush remains unchanged, and the rest of the red is converted to blue.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID Example_SetClearBrushRemap(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"TestMetafile4.emf");
   ImageAttributes imAtt;

   ColorMap defaultMap;
   defaultMap.oldColor = Color(255, 255, 0, 0);   // red converted to blue
   defaultMap.newColor = Color(255, 0, 0, 255);

   ColorMap brushMap;
   brushMap.oldColor = Color(255, 255, 0, 0);     // red converted to green
   brushMap.newColor = Color(255, 0, 255, 0);

   // Set the default color-remap table.
   imAtt.SetRemapTable(1, &amp;defaultMap, ColorAdjustTypeDefault);

   // Draw the image (metafile) using no color adjustment.
   graphics.DrawImage(
      &amp;image,
      Rect(10, 10, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel);

   // Draw the image (metafile) using default color adjustment.
   // All red is converted to blue.
   graphics.DrawImage(
      &amp;image,
      Rect(10, 90, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &amp;imAtt);

   // Set the brush remap table.
   imAtt.SetBrushRemapTable(1, &amp;brushMap);

   // Draw the image (metafile) using default and brush adjustment.
   // Red painted with a brush is converted to green.
   // All other red is converted to blue (default).
   graphics.DrawImage(
      &amp;image,
      Rect(10, 170, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),           // source rect
      UnitPixel,
      &amp;imAtt);

   // Clear the brush remap table.
   imAtt.ClearBrushRemapTable();

   // Draw the image (metafile) using only default color adjustment.
   // Red painted with a brush gets no color adjustment.
   // All other red is converted to blue (default).
   graphics.DrawImage(
      &amp;image,
      Rect(10, 250, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),           // source rect
      UnitPixel,
      &amp;imAtt);  
}
				</pre>
</td>
</tr>
</table></span></div>
The preceding code, along with a particular file, Testmetafile4.emf, produced the following output. The ellipses in the left column were drawn with a pen, and the ellipses in the right column were filled with a brush. Note that the default remap table applies to the ellipses drawn with a pen. The remap table that applies to the ellipses filled with a brush varies according to the <a href="https://msdn.microsoft.com/en-us/library/ms535428(v=VS.85).aspx">ImageAttributes::SetBrushRemapTable</a> and <b>ImageAttributes::ClearBrushRemapTable</b> calls.

<img alt="Illustration showing four empty ellipses; the first is red and the rest blue, then four filled ellipses: red, blue, green, and red" src="./images/imageattributesclearbrushremap.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534062(v=VS.85).aspx">ColorMap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535422(v=VS.85).aspx">ImageAttributes::ClearRemapTable</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535428(v=VS.85).aspx">ImageAttributes::SetBrushRemapTable</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535436(v=VS.85).aspx">ImageAttributes::SetRemapTable</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

