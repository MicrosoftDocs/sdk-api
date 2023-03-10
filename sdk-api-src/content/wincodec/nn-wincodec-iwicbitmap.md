---
UID: NN:wincodec.IWICBitmap
title: IWICBitmap (wincodec.h)
description: Defines methods that add the concept of writeability and static in-memory representations of bitmaps to IWICBitmapSource.
helpviewer_keywords: ["IWICBitmap","IWICBitmap interface [Windows Imaging Component]","IWICBitmap interface [Windows Imaging Component]","described","_wic_codec_iwicbitmap","wic._wic_codec_iwicbitmap","wincodec/IWICBitmap"]
old-location: wic\_wic_codec_iwicbitmap.htm
tech.root: wic
ms.assetid: 15dcc80d-ef58-453d-a57a-348ffc7ddc6b
ms.date: 12/05/2018
ms.keywords: IWICBitmap, IWICBitmap interface [Windows Imaging Component], IWICBitmap interface [Windows Imaging Component],described, _wic_codec_iwicbitmap, wic._wic_codec_iwicbitmap, wincodec/IWICBitmap
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmap
 - wincodec/IWICBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmap
---

# IWICBitmap interface


## -description

Defines methods that add the concept of writeability and static in-memory representations of bitmaps to <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>.

## -inheritance

The <b>IWICBitmap</b> interface inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>. <b>IWICBitmap</b> also has these types of members:

## -remarks

<b>IWICBitmap</b> inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> and therefore also inherits the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a> method.
            When pixels need to be moved to a new memory location, <b>CopyPixels</b> is often the most efficient.
         

Because of the internal memory representation implied by the <b>IWICBitmap</b>, in-place modification and processing using the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-lock">Lock</a> is more efficient than <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a>, usually reducing to a simple pointer access directly into the memory owned by the bitmap rather than a copy. 
            This is contrasted to procedural bitmaps which implement only <b>CopyPixels</b> because there is no internal memory representation and one would need to be created on demand to satisfy a call to <b>Lock</b>.
