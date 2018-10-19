---
UID: NF:gdiplusimageattributes.ImageAttributes.SetOutputChannel
title: ImageAttributes::SetOutputChannel
author: windows-sdk-content
description: The ImageAttributes::SetOutputChannel method sets the CMYK output channel for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetOutputChannel_channelFlags_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setoutputchannel.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ImageAttributes class [GDI+],SetOutputChannel method, ImageAttributes.SetOutputChannel, ImageAttributes::SetOutputChannel, SetOutputChannel, SetOutputChannel method [GDI+], SetOutputChannel method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetOutputChannel_channelFlags_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetOutputChannel_channelFlags_type_
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
 - ImageAttributes.SetOutputChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetOutputChannel


## -description


The <b>ImageAttributes::SetOutputChannel</b> method sets the CMYK output channel for a specified category.


## -parameters




### -param channelFlags [in]

Type: <b><a href="https://msdn.microsoft.com/bb71bdc3-8ebe-4acd-959e-482037806598">ColorChannelFlags</a></b>

Element of the <a href="https://msdn.microsoft.com/bb71bdc3-8ebe-4acd-959e-482037806598">ColorChannelFlags</a> enumeration that specifies the output channel. 


### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a> enumeration that specifies the category for which the output channel is set. The default value is <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



You can use the <b>ImageAttributes::SetOutputChannel</b> method to convert an image to a cyan-magenta-yellow-black (CMYK) color space and examine the intensities of one of the CMYK color channels. For example, suppose you create an <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object and set its bitmap output channel to <a href="https://msdn.microsoft.com/bb71bdc3-8ebe-4acd-959e-482037806598">ColorChannelFlagsC</a>. If you pass the address of that <b>ImageAttributes</b> object to the <a href="https://msdn.microsoft.com/ec2eb9c8-e5f1-4f0d-968f-e4ac16d670d6">DrawImage</a> method, the cyan component of each pixel is calculated, and each pixel in the rendered image is a shade of gray that indicates the intensity of its cyan channel. Similarly, you can render images that indicate the intensities of the magenta, yellow, and black channels.

An <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify an output channel for the default category and a different output channel for the bitmap category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the bitmap category, then the default settings apply to the bitmap category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the output channel for the bitmap category by passing <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeBitmap</a> to the <b>ImageAttributes::SetOutputChannel</b> method, then none of the default adjustment settings will apply to bitmaps.


#### Examples



The following example creates an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object and calls the <a href="https://msdn.microsoft.com/ec2eb9c8-e5f1-4f0d-968f-e4ac16d670d6">DrawImage</a> method to draw the image. Then the code creates an <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object and sets its bitmap output channel to cyan (<a href="https://msdn.microsoft.com/bb71bdc3-8ebe-4acd-959e-482037806598">ColorChannelFlagsC</a>). The code calls <a href="https://msdn.microsoft.com/7864f9f6-40c0-428c-8867-2a37abed0505">DrawImage</a> a second time, passing the address of the <b>Image</b> object and the address of the <b>ImageAttributes</b> object. The cyan channel of each pixel is calculated, and the rendered image shows the intensities of the cyan channel as shades of gray. The code calls <b>DrawImage</b> three more times to show the intensities of the magenta, yellow, and black channels.


```cpp

VOID Example_SetOutputChannel(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"Mosaic2.bmp");

   // Draw the image unaltered.
   graphics.DrawImage(&image, 10, 10, width, height);

   UINT width = image.GetWidth();
   UINT height = image.GetHeight();

   ImageAttributes imAtt;

   // Draw the image, showing the intensity of the cyan channel.
   imAtt.SetOutputChannel(ColorChannelFlagsC, ColorAdjustTypeBitmap);
   graphics.DrawImage(
      &image,
      Rect(110, 10, width, height),  // dest rect
      0, 0, width, height,           // source rect
      UnitPixel,
      &imAtt);

   // Draw the image, showing the intensity of the magenta channel.
   imAtt.SetOutputChannel(ColorChannelFlagsM, ColorAdjustTypeBitmap);
   graphics.DrawImage(
      &image,
      Rect(210, 10, width, height),  // dest rect
      0, 0, width, height,           // source rect
      UnitPixel,
      &imAtt);

   // Draw the image, showing the intensity of the yellow channel.
   imAtt.SetOutputChannel(ColorChannelFlagsY, ColorAdjustTypeBitmap);
   graphics.DrawImage(
      &image,
      Rect(10, 110, width, height),  // dest rect
      0, 0, width, height,           // source rect
      UnitPixel,
      &imAtt);

   // Draw the image, showing the intensity of the black channel.
   imAtt.SetOutputChannel(ColorChannelFlagsK, ColorAdjustTypeBitmap);
   graphics.DrawImage(
      &image,
      Rect(110, 110, width, height),  // dest rect
      0, 0, width, height,            // source rect
      UnitPixel,
      &imAtt); 
}
				
```


The following illustration shows the output of the preceding code.

<img alt="Illustration showing five versions of one image: first in color, then in four different patterns of greyscale" src="./images/imageattributessetoutputchannel.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/bb71bdc3-8ebe-4acd-959e-482037806598">ColorChannelFlags</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/63557a4a-834f-4914-8179-d66ca3585ecf">ImageAttributes::ClearOutputChannel</a>



<a href="https://msdn.microsoft.com/100aee97-6567-4458-9c2e-9906ab0c4ece">ImageAttributes::ClearOutputChannelColorProfile</a>



<a href="https://msdn.microsoft.com/b5e466d7-e2e1-471c-be05-a587b65556af">ImageAttributes::SetOutputChannelColorProfile</a>
 

 

