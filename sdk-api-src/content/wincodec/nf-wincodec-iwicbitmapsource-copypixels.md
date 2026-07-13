---
UID: NF:wincodec.IWICBitmapSource.CopyPixels
title: IWICBitmapSource::CopyPixels (wincodec.h)
description: Instructs the object to produce pixels.
helpviewer_keywords: ["CopyPixels","CopyPixels method [Windows Imaging Component]","CopyPixels method [Windows Imaging Component]","IWICBitmapSource interface","IWICBitmapSource interface [Windows Imaging Component]","CopyPixels method","IWICBitmapSource.CopyPixels","IWICBitmapSource::CopyPixels","_wic_codec_iwicbitmapsource_copypixels","wic._wic_codec_iwicbitmapsource_copypixels","wincodec/IWICBitmapSource::CopyPixels"]
old-location: wic\_wic_codec_iwicbitmapsource_copypixels.htm
tech.root: wic
ms.assetid: d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c
ms.date: 12/05/2018
ms.keywords: CopyPixels, CopyPixels method [Windows Imaging Component], CopyPixels method [Windows Imaging Component],IWICBitmapSource interface, IWICBitmapSource interface [Windows Imaging Component],CopyPixels method, IWICBitmapSource.CopyPixels, IWICBitmapSource::CopyPixels, _wic_codec_iwicbitmapsource_copypixels, wic._wic_codec_iwicbitmapsource_copypixels, wincodec/IWICBitmapSource::CopyPixels
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
 - IWICBitmapSource::CopyPixels
 - wincodec/IWICBitmapSource::CopyPixels
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
 - IWICBitmapSource.CopyPixels
---

# IWICBitmapSource::CopyPixels


## -description

Instructs the object to produce pixels.

## -parameters

### -param prc [in]

Type: <b>const <a href="/windows/desktop/api/wincodec/ns-wincodec-wicrect">WICRect</a>*</b>

The rectangle to copy. A <b>NULL</b> value specifies the entire bitmap.

### -param cbStride [in]

Type: <b>UINT</b>

The stride of the bitmap

### -param cbBufferSize [in]

Type: <b>UINT</b>

The size of the buffer.

### -param pbBuffer [out]

Type: <b>BYTE*</b>

A pointer to the buffer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>CopyPixels</b> is one of the two main image processing routines (the other being <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-lock">Lock</a>) triggering the actual processing. 
         It instructs the object to produce pixels according to its algorithm - this may involve decoding a portion of a JPEG stored on disk, copying a block of memory, or even analytically computing a complex gradient. 
         The algorithm is completely dependent on the object implementing the interface.
      

The caller can restrict the operation to a rectangle of interest (ROI) using the prc parameter. 
         The ROI sub-rectangle must be fully contained in the bounds of the bitmap. 
         Specifying a <b>NULL</b> ROI implies that the whole bitmap should be returned. 


The caller controls the memory management and must provide an output buffer (<i>pbBuffer</i>) for the results of the copy along with the buffer's bounds (<i>cbBufferSize</i>). 
         The cbStride parameter defines the count of bytes between two vertically adjacent pixels in the output buffer. 
         The caller must ensure that there is sufficient buffer to complete the call based on the width, height and pixel format of the bitmap and the sub-rectangle provided to the copy method.
      

If the caller needs to perform numerous copies of an expensive <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> such as a JPEG, it is recommended to create an in-memory <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> first.
      

<h3><a id="Codec_Developer_Remarks"></a><a id="codec_developer_remarks"></a><a id="CODEC_DEVELOPER_REMARKS"></a>Codec Developer Remarks</h3>
The callee must only write to the first (prc-&gt;Width*bitsperpixel+7)/8 bytes of each line of the output buffer (in this case, a line is a consecutive string of <i>cbStride</i> bytes).