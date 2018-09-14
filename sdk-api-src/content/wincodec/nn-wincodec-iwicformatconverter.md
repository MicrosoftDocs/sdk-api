---
UID: NN:wincodec.IWICFormatConverter
title: IWICFormatConverter
author: windows-sdk-content
description: Represents an IWICBitmapSource that converts the image data from one pixel format to another, handling dithering and halftoning to indexed formats, palette translation and alpha thresholding.
old-location: wic\_wic_codec_iwicformatconverter.htm
tech.root: wic
ms.assetid: d558aaa7-5962-424c-9e83-363fba09ad50
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWICFormatConverter, IWICFormatConverter interface [Windows Imaging Component], IWICFormatConverter interface [Windows Imaging Component],described, _wic_codec_iwicformatconverter, wic._wic_codec_iwicformatconverter, wincodec/IWICFormatConverter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICFormatConverter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICFormatConverter interface


## -description


Represents an <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> that converts the image data from one pixel format to another, handling dithering and halftoning to indexed formats, palette translation and alpha thresholding.
         


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICFormatConverter</b> interface inherits from <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>. <b>IWICFormatConverter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICFormatConverter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf813eaf-0899-4df2-bcc2-ba2db1e9af2f">CanConvert</a>
</td>
<td align="left" width="63%">
Determines if the source pixel format can be converted to the destination pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff046b2c-a863-48dd-9cbe-3c559c84b682">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the format converter.

</td>
</tr>
</table> 


## -see-also




<a href="f6a44610-0d30-420e-aaf9-c7f436f3c195">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>



<a href="https://msdn.microsoft.com/a05b496a-bd4c-4065-8060-df0f8930cde7">Windows Imaging Component Overview</a>
 

 

