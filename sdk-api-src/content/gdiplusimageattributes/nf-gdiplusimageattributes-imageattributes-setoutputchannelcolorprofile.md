---
UID: NF:gdiplusimageattributes.ImageAttributes.SetOutputChannelColorProfile
title: ImageAttributes::SetOutputChannelColorProfile
author: windows-sdk-content
description: The ImageAttributes::SetOutputChannelColorProfile method sets the output channel color-profile file for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetOutputChannelColorProfile_colorProfileFilename_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setoutputchannelcolorprofile.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ImageAttributes class [GDI+],SetOutputChannelColorProfile method, ImageAttributes.SetOutputChannelColorProfile, ImageAttributes::SetOutputChannelColorProfile, SetOutputChannelColorProfile, SetOutputChannelColorProfile method [GDI+], SetOutputChannelColorProfile method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetOutputChannelColorProfile_colorProfileFilename_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetOutputChannelColorProfile_colorProfileFilename_type_
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
 - ImageAttributes.SetOutputChannelColorProfile
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetOutputChannelColorProfile


## -description


The <b>ImageAttributes::SetOutputChannelColorProfile</b> method sets the output channel color-profile file for a specified category.


## -parameters




### -param colorProfileFilename [in]

Type: <b>const WCHAR*</b>

Path name of a color-profile file. If the color-profile file is in the %SystemRoot%\System32\Spool\Drivers\Color directory, then this parameter can be the file name. Otherwise, this parameter must be the fully qualified path name. 


### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the output channel color-profile file is set. The default value is <a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



You can use the <a href="https://msdn.microsoft.com/library/ms535434(v=VS.85).aspx">ImageAttributes::SetOutputChannel</a> and <b>ImageAttributes::SetOutputChannelColorProfile</b> methods to convert an image to a cyan-magenta-yellow-black (CMYK) color space and examine the intensities of one of the CMYK color channels. For example, suppose you write code that performs the following steps: 

<ol>
<li>Create an <a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a> object. </li>
<li>Create an <a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. </li>
<li>Pass <a href="https://msdn.microsoft.com/library/ms534090(v=VS.85).aspx">ColorChannelFlagsC</a> to the <a href="https://msdn.microsoft.com/library/ms535434(v=VS.85).aspx">ImageAttributes::SetOutputChannel</a> method of the 
						<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. </li>
<li>Pass the path name of a color profile file to the <b>ImageAttributes::SetOutputChannelColorProfile</b> method of the 
						<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. </li>
<li>Pass the addresses of the <a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a> and 
						<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> objects to the <a href="https://msdn.microsoft.com/library/ms536030(v=VS.85).aspx">DrawImage</a> method. </li>
</ol>
Windows GDI+ will use the color-profile file to calculate the cyan component of each pixel in the image, and each pixel in the rendered image will be a shade of gray that indicates the intensity of its cyan channel.

An 
				<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify an output channel color-profile file for the default category and a different output channel color-profile file for the bitmap category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the bitmap category, then the default settings apply to the bitmap category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the output channel color-profile file for the bitmap category by passing <a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustTypeBitmap</a> to the <b>ImageAttributes::SetOutputChannelColorProfile</b> method, then none of the default adjustment settings will apply to bitmaps.


#### Examples



The following example creates an <a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a> object and calls the <a href="https://msdn.microsoft.com/library/ms536030(v=VS.85).aspx">DrawImage</a> method to draw the image. Then the code creates an 
						<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object and calls its <b>ImageAttributes::SetOutputChannelColorProfile</b> method to specify a profile file for the bitmap category. The call to <a href="https://msdn.microsoft.com/library/ms535434(v=VS.85).aspx">ImageAttributes::SetOutputChannel</a> sets the output channel (for the bitmap category) to cyan. The code calls <b>DrawImage</b> a second time, passing the address of the <b>Image</b> object and the address of the <b>ImageAttributes</b> object. The cyan channel of each pixel is calculated, and the rendered image shows the intensities of the cyan channel as shades of gray. The code calls <b>DrawImage</b> three more times to show the intensities of the magenta, yellow, and black channels.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID Example_SetOutputProfile(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"Mosaic2.bmp");
   ImageAttributes imAtt;
   UINT width = image.GetWidth();
   UINT height = image.GetHeight();

   // Draw the image unaltered.
   graphics.DrawImage(&amp;image, 10, 10, width, height);

   imAtt.SetOutputChannelColorProfile(
      L"TEKPH600.ICM", ColorAdjustTypeBitmap);

   // Draw the image, showing the intensity of the cyan channel.
   imAtt.SetOutputChannel(ColorChannelFlagsC, ColorAdjustTypeBitmap);
   graphics.DrawImage(
      &amp;image,
      Rect(110, 10, width, height),  // dest rect
      0, 0, width, height,           // source rect
      UnitPixel,
      &amp;imAtt);

   // Draw the image, showing the intensity of the magenta channel.
   imAtt.SetOutputChannel(ColorChannelFlagsM, ColorAdjustTypeBitmap);
   graphics.DrawImage(
      &amp;image,
      Rect(210, 10, width, height),  // dest rect
      0, 0, width, height,           // source rect
      UnitPixel,
      &amp;imAtt);

   // Draw the image, showing the intensity of the yellow channel.
   imAtt.SetOutputChannel(ColorChannelFlagsY, ColorAdjustTypeBitmap);
   graphics.DrawImage(
      &amp;image,
      Rect(10, 110, width, height),  // dest rect
      0, 0, width, height,           // source rect
      UnitPixel,
      &amp;imAtt);

   // Draw the image, showing the intensity of the black channel.
   imAtt.SetOutputChannel(ColorChannelFlagsK, ColorAdjustTypeBitmap);
   graphics.DrawImage(
      &amp;image,
      Rect(110, 110, width, height),  // dest rect
      0, 0, width, height,            // source rect
      UnitPixel,
      &amp;imAtt); 
}
				</pre>
</td>
</tr>
</table></span></div>
The preceding code, along with the files Mosaic2.bmp and Tekph600.icm, produced the following output.

<img alt="Illustration showing four versions of one image: first in color, then in three different patterns of greyscale" src="./images/imageattributessetoutputprofile.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/library/ms534090(v=VS.85).aspx">ColorChannelFlags</a>



<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/library/ms535420(v=VS.85).aspx">ImageAttributes::ClearOutputChannel</a>



<a href="https://msdn.microsoft.com/library/ms535421(v=VS.85).aspx">ImageAttributes::ClearOutputChannelColorProfile</a>



<a href="https://msdn.microsoft.com/library/ms535434(v=VS.85).aspx">ImageAttributes::SetOutputChannel</a>
 

 

