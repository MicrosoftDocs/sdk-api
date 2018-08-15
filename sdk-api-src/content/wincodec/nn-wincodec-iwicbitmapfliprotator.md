---
UID: NN:wincodec.IWICBitmapFlipRotator
title: IWICBitmapFlipRotator
author: windows-sdk-content
description: Exposes methods that produce a flipped (horizontal or vertical) and/or rotated (by 90 degree increments) bitmap source. Rotations are done before the flip.
old-location: wic\_wic_codec_iwicbitmapfliprotator.htm
old-project: wic
ms.assetid: 1fcb19ba-34bd-48c0-9964-0c973c31cacc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWICBitmapFlipRotator, IWICBitmapFlipRotator interface [Windows Imaging Component], IWICBitmapFlipRotator interface [Windows Imaging Component],described, _wic_codec_iwicbitmapfliprotator, wic._wic_codec_iwicbitmapfliprotator, wincodec/IWICBitmapFlipRotator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapFlipRotator
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapFlipRotator interface


## -description


Exposes methods that produce a flipped (horizontal or vertical) and/or rotated (by 90 degree increments) bitmap source. Rotations are done before the flip.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapFlipRotator</b> interface inherits from <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>. <b>IWICBitmapFlipRotator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapFlipRotator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c70d25d-b591-4ef4-91b5-b8350da99df1">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the bitmap flip rotator with the provided parameters.

</td>
</tr>
</table> 


## -remarks



IWICBitmapFipRotator requests data on a per-pixel basis, while WIC codecs provide data on a per-scanline basis. This causes the fliprotator object to exhibit n² behavior if there is no buffering.  This occures because each pixel in the transformed image requires an entire scanline to be decoded in the file. It is recommended that you buffer the image using <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>, or flip/rotate the image using Direct2D.



