---
UID: NF:gdiplusimageattributes.ImageAttributes.SetRemapTable
title: ImageAttributes::SetRemapTable
author: windows-sdk-content
description: The ImageAttributes::SetRemapTable method sets the color-remap table for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetRemapTable_mapSize_map_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setremaptable.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ImageAttributes class [GDI+],SetRemapTable method, ImageAttributes.SetRemapTable, ImageAttributes::SetRemapTable, SetRemapTable, SetRemapTable method [GDI+], SetRemapTable method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetRemapTable_mapSize_map_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetRemapTable_mapSize_map_type_
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ImageAttributes.SetRemapTable
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetRemapTable


## -description


The <b>ImageAttributes::SetRemapTable</b> method sets the color-remap table for a specified category.


## -parameters




### -param mapSize [in]

Type: <b>UINT</b>

<b>INT</b> that specifies the number of elements in the <i>map</i> array. 


### -param map [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms534062(v=VS.85).aspx">ColorMap</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/library/ms534062(v=VS.85).aspx">ColorMap</a> structures that defines the color map. 


### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the color-remap table is set. The default value is <a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A color-remap table is an array of <a href="https://msdn.microsoft.com/library/ms534062(v=VS.85).aspx">ColorMap</a> structures. Each <b>ColorMap</b> structure has two <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> objects: one that specifies an old color and one that specifies a corresponding new color. During rendering, any color that matches one of the old colors in the remap table is changed to the corresponding new color.

An <a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color remap for the default category, a color-remap table for the bitmap category, and still a different color-remap table for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the color-remap table for the pen category by passing <a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetRemapTable</b> method, then none of the default adjustment settings will apply to pens.


#### Examples



The following example creates an <a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a> object based on a .bmp file and then draws the image. The code creates an <a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object and sets its default remap table so that red is converted to blue. Then the code draws the image again using the color adjustment specified by the remap table.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID Example_SetRemapTable(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an Image object based on a .bmp file.
   // The image has one red stripe and one green stripe.
   Image image(L"RedGreenStripes.bmp");

   // Create an ImageAttributes object and set its remap table.
   ImageAttributes imageAtt;
   ColorMap cMap;
   cMap.oldColor = Color(255, 255, 0, 0);  // red 
   cMap.newColor = Color(255, 0, 0, 255);  // blue
   imageAtt.SetRemapTable(12, &amp;cMap,
      ColorAdjustTypeDefault);

   // Draw the image with no color adjustment.
   graphics.DrawImage(&amp;image, 10, 10, image.GetWidth(), image.GetHeight());
 
   // Draw the image with red converted to blue.
   graphics.DrawImage(&amp;image,
      Rect(100, 10, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),           // source rect
      UnitPixel,
      &amp;imageAtt);
}
				</pre>
</td>
</tr>
</table></span></div>
The following illustration shows the output of the preceding code.

<img alt="Illustration showing a rectangle with red and green regions, then the same rectangle with the red region replaced with blue" src="./images/imageattributessetremaptable.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/library/ms534062(v=VS.85).aspx">ColorMap</a>



<a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/library/ms535422(v=VS.85).aspx">ImageAttributes::ClearRemapTable</a>



<a href="https://msdn.microsoft.com/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

