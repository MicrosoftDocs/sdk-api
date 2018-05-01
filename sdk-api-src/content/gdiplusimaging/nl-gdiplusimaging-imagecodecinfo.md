---
UID: NL:gdiplusimaging.ImageCodecInfo
title: ImageCodecInfo
author: windows-driver-content
description: An ImageCodecInfo object stores information about an image codec (encoder/decoder).
old-location: gdiplus\_gdiplus_CLASS_ImageCodecInfo_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imagecodecinfo.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ImageCodecInfo, ImageCodecInfo class [GDI+], ImageCodecInfo class [GDI+], described, _gdiplus_CLASS_ImageCodecInfo_Class, gdiplus._gdiplus_CLASS_ImageCodecInfo_Class, gdiplusimaging/ImageCodecInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: gdiplusimaging.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.lib
-	Gdiplus.dll
api_name:
-	ImageCodecInfo
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# ImageCodecInfo class


## -description


An <b>ImageCodecInfo</b> object stores information about an image codec (encoder/decoder). GDI+ provides several built-in image codecs. You can obtain information about those codecs by calling the 
			<a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a> function and the 
			<a href="https://msdn.microsoft.com/ea9f1436-dafe-4e0d-8cca-81ec262d06a5">GetImageDecoders</a> function. Each of those functions returns an array of <b>ImageCodecInfo</b> objects, one for each available encoder or decoder.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">ImageCodecInfo</b> has these types of members:


## -see-also




<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a>



<a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a>



<a href="https://msdn.microsoft.com/2a7f40dc-1132-429b-bc44-79f28c9098d7">Image::GetEncoderParameterList</a>



<a href="https://msdn.microsoft.com/f7b0f80c-8fff-4fb7-bd7d-0b82275bd92d">Image::GetEncoderParameterListSize</a>



<a href="https://msdn.microsoft.com/a261cf61-b853-4208-984b-0d5040eb1667">Listing Installed Encoders</a>



<a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a>
 

 

