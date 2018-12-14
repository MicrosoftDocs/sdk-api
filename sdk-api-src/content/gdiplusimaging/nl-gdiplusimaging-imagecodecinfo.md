---
UID: NL:gdiplusimaging.ImageCodecInfo
title: ImageCodecInfo
author: windows-sdk-content
description: An ImageCodecInfo object stores information about an image codec (encoder/decoder).
old-location: gdiplus\_gdiplus_CLASS_ImageCodecInfo_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imagecodecinfo.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImageCodecInfo, ImageCodecInfo class [GDI+], ImageCodecInfo class [GDI+],described, _gdiplus_CLASS_ImageCodecInfo_Class, gdiplus._gdiplus_CLASS_ImageCodecInfo_Class, gdiplusimaging/ImageCodecInfo
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
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - ImageCodecInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageCodecInfo class


## -description


An <b>ImageCodecInfo</b> object stores information about an image codec (encoder/decoder). GDI+ provides several built-in image codecs. You can obtain information about those codecs by calling the 
			<a href="https://msdn.microsoft.com/en-us/library/ms534080(v=VS.85).aspx">GetImageEncoders</a> function and the 
			<a href="https://msdn.microsoft.com/en-us/library/ms534078(v=VS.85).aspx">GetImageDecoders</a> function. Each of those functions returns an array of <b>ImageCodecInfo</b> objects, one for each available encoder or decoder.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">ImageCodecInfo</b> has these types of members:


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534434(v=VS.85).aspx">EncoderParameter</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535374(v=VS.85).aspx">Image::GetEncoderParameterList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535375(v=VS.85).aspx">Image::GetEncoderParameterListSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533842(v=VS.85).aspx">Listing Installed Encoders</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533814(v=VS.85).aspx">Using Image Encoders and Decoders</a>
 

 

