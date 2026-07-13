---
UID: NF:wincodec.IWICBitmapEncoder.Commit
title: IWICBitmapEncoder::Commit (wincodec.h)
description: Commits all changes for the image and closes the stream.
helpviewer_keywords: ["Commit","Commit method [Windows Imaging Component]","Commit method [Windows Imaging Component]","IWICBitmapEncoder interface","IWICBitmapEncoder interface [Windows Imaging Component]","Commit method","IWICBitmapEncoder.Commit","IWICBitmapEncoder::Commit","_wic_codec_iwicbitmapencoder_commit","wic._wic_codec_iwicbitmapencoder_commit","wincodec/IWICBitmapEncoder::Commit"]
old-location: wic\_wic_codec_iwicbitmapencoder_commit.htm
tech.root: wic
ms.assetid: 97e39e73-3494-4679-8962-eb48242f9b9f
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Windows Imaging Component], Commit method [Windows Imaging Component],IWICBitmapEncoder interface, IWICBitmapEncoder interface [Windows Imaging Component],Commit method, IWICBitmapEncoder.Commit, IWICBitmapEncoder::Commit, _wic_codec_iwicbitmapencoder_commit, wic._wic_codec_iwicbitmapencoder_commit, wincodec/IWICBitmapEncoder::Commit
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
 - IWICBitmapEncoder::Commit
 - wincodec/IWICBitmapEncoder::Commit
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
 - IWICBitmapEncoder.Commit
---

# IWICBitmapEncoder::Commit


## -description

Commits all changes for the image and closes the stream.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To finalize an image, both the frame <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-commit">Commit</a> and the encoder <b>Commit</b> must be called. However, only call the encoder  <b>Commit</b> method after all frames have been committed.

After the encoder has been committed, it can't be re-initialized or reused with another stream. A new encoder interface must be created, for example, with <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createencoder">IWICImagingFactory::CreateEncoder</a>.


For the encoder <b>Commit</b> to succeed, you must at a minimum call  <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-initialize">IWICBitmapEncoder::Initialize</a> and either <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writesource">IWICBitmapFrameEncode::WriteSource</a> or <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writepixels">IWICBitmapFrameEncode::WritePixels</a>.



<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writesource">IWICBitmapFrameEncode::WriteSource</a> specifies all parameters needed to encode the image data. <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writepixels">IWICBitmapFrameEncode::WritePixels</a> requires that you also call <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setsize">IWICBitmapFrameEncode::SetSize</a>, <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat">IWICBitmapFrameEncode::SetPixelFormat</a>, and <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setpalette">IWICBitmapFrameEncode::SetPalette</a> (if the pixel format is indexed).

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-commit">Commit</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a>
