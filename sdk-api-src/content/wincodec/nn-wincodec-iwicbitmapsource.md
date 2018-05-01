---
UID: NN:wincodec.IWICBitmapSource
title: IWICBitmapSource
author: windows-driver-content
description: Exposes methods that refers to a source from which pixels are retrieved, but cannot be written back to.
old-location: wic\_wic_codec_iwicbitmapsource.htm
old-project: wic
ms.assetid: abcc84af-6067-4856-8618-fb66aff4255a
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IWICBitmapSource, IWICBitmapSource interface [Windows Imaging Component], IWICBitmapSource interface [Windows Imaging Component], described, _wic_codec_iwicbitmapsource, wic._wic_codec_iwicbitmapsource, wincodec/IWICBitmapSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICBitmapSource
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapSource interface


## -description


Exposes methods that refers to a source from which pixels are retrieved, but cannot be written back to.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICBitmapSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e45ca4a-2d14-4829-9542-9cfc3e4b0d73">CopyPalette</a>
</td>
<td align="left" width="63%">
Retrieves the color table for indexed pixel formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">CopyPixels</a>
</td>
<td align="left" width="63%">
Instructs the object to produce pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fd30a38-a447-4e4e-93ea-e31c5ba1271e">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Retrieves the pixel format of the bitmap source.. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49241ed1-1036-4f88-9116-4727de883b3e">GetResolution</a>
</td>
<td align="left" width="63%">
Retrieves the sampling rate between pixels and physical world measurements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fba35fd-288c-4095-83b8-d2320dc5916c">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the pixel width and height of the bitmap.

</td>
</tr>
</table> 


## -remarks



This interface provides a common way of accessing and linking together bitmaps, decoders, format converters, and scalers. Components that implement this interface can be connected together in a graph to pull imaging data through.

This interface defines only the notion of readability or being able to produce pixels. Modifying or writing to a bitmap is considered to be a specialization specific to bitmaps which have storage and is defined in the descendant interface <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>.




## -see-also




<a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>
 

 

