---
UID: NF:gdiplusimageattributes.ImageAttributes.SetColorKey
title: ImageAttributes::SetColorKey
author: windows-sdk-content
description: The ImageAttributes::SetColorKey method sets the color key (transparency range) for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetColorKey_colorLow_colorHigh_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setcolorkey.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImageAttributes class [GDI+],SetColorKey method, ImageAttributes.SetColorKey, ImageAttributes::SetColorKey, SetColorKey, SetColorKey method [GDI+], SetColorKey method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetColorKey_colorLow_colorHigh_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetColorKey_colorLow_colorHigh_type_
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
 - ImageAttributes.SetColorKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetColorKey


## -description


The <b>ImageAttributes::SetColorKey</b> method sets the color key (transparency range) for a specified category. 


## -parameters




### -param colorLow [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a> object that specifies the low color-key value. 


### -param colorHigh [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a> object that specifies the high color-key value.


### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the color key is set. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



This method sets the high and low color-key values so that arange of colors can be made transparent. Any color that has each of its three components (red, green, blue) between the corresponding components of the high and low color keys is made transparent.

An 
				<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color key for the default category, a different color key for the bitmap category, and still a different color key for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the color key for the pen category by passing <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetColorKey</b> method, then none of the default adjustment settings will apply to pens.


#### Examples



The following example creates an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object from a .bmp file. The code also creates an 
						<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. The call to <b>ImageAttributes::SetColorKey</b> sets the bitmap color key of the 
						<b>ImageAttributes</b> object so that any color that satisfies all three of the following conditions is made transparent: 
						<ul>
<li>The red component is in the range 100 through 250.</li>
<li>The green component is in the range 95 through 245.</li>
<li>The blue component is in the range 30 through 60.</li>
</ul>


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID Example_SetColorKey(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an Image object based on a BMP file.
   // The image has three horizontal stripes.
   // The color of the top stripe has RGB components (90, 90, 20).
   // The color of the middle stripe has RGB components (150, 150, 150).
   // The color of the bottom stripe has RGB components (130, 130, 40).
   Image image(L"ColorKeyTest.bmp");

   // Create an ImageAttributes object, and set its color key.
   ImageAttributes imAtt;
   imAtt.SetColorKey(
      Color(100, 95, 30),
      Color(250, 245, 60),
      ColorAdjustTypeBitmap);

   // Draw the image. Apply the color key.
   // The bottom stripe of the image will be transparent because
   // 100 &lt;= 130 &lt;= 250 and
   // 95  &lt;= 130 &lt;= 245 and
   // 30  &lt;= 40  &lt;= 60.
   graphics.DrawImage(
      &amp;image, 
      Rect(20, 20, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &amp;imAtt);
}
				</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535415(v=VS.85).aspx">ImageAttributes::ClearColorKey</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535423(v=VS.85).aspx">ImageAttributes::ClearThreshold</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535437(v=VS.85).aspx">ImageAttributes::SetThreshold</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

