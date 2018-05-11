---
UID: NN:wincodec.IWICBitmap
title: IWICBitmap
author: windows-driver-content
description: Defines methods that add the concept of writeability and static in-memory representations of bitmaps to IWICBitmapSource.
old-location: wic\_wic_codec_iwicbitmap.htm
old-project: wic
ms.assetid: 15dcc80d-ef58-453d-a57a-348ffc7ddc6b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWICBitmap, IWICBitmap interface [Windows Imaging Component], IWICBitmap interface [Windows Imaging Component],described, _wic_codec_iwicbitmap, wic._wic_codec_iwicbitmap, wincodec/IWICBitmap
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
-	IWICBitmap
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmap interface


## -description


Defines methods that add the concept of writeability and static in-memory representations of bitmaps to <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmap</b> interface inherits from <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>. <b>IWICBitmap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ab25a00-c89c-4a2c-8e12-8ce81cc21bca">Lock</a>
</td>
<td align="left" width="63%">
Provides access to a rectangular area of the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a46c968e-9ff0-479e-8f98-0d2fbbc5d6b0">SetPalette</a>
</td>
<td align="left" width="63%">
Provides access for palette modifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8b6c600-0ef0-4fa7-a70f-0299e640c196">SetResolution</a>
</td>
<td align="left" width="63%">
Changes the physical resolution of the image.

</td>
</tr>
</table> 


## -remarks



<b>IWICBitmap</b> inherits from <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> and therefore also inherits the <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">CopyPixels</a> method.
            When pixels need to be moved to a new memory location, <b>CopyPixels</b> is often the most efficient.
         


            Because of to the internal memory representation implied by the <b>IWICBitmap</b>, in-place modification and processing using the <a href="https://msdn.microsoft.com/2ab25a00-c89c-4a2c-8e12-8ce81cc21bca">Lock</a> is more efficient than <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">CopyPixels</a>, usually reducing to a simple pointer access directly into the memory owned by the bitmap rather than a as a copy. 
            This is contrasted to procedural bitmaps which implement only <b>CopyPixels</b> because there is no internal memory representation and one would need to be created on demand to satisfy a call to <b>Lock</b>. 
         



