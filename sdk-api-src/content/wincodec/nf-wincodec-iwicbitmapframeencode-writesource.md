---
UID: NF:wincodec.IWICBitmapFrameEncode.WriteSource
title: IWICBitmapFrameEncode::WriteSource (wincodec.h)
description: Encodes a bitmap source.
helpviewer_keywords: ["IWICBitmapFrameEncode interface [Windows Imaging Component]","WriteSource method","IWICBitmapFrameEncode.WriteSource","IWICBitmapFrameEncode::WriteSource","WriteSource","WriteSource method [Windows Imaging Component]","WriteSource method [Windows Imaging Component]","IWICBitmapFrameEncode interface","_wic_codec_iwicbitmapframeencode_writesource","wic._wic_codec_iwicbitmapframeencode_writesource","wincodec/IWICBitmapFrameEncode::WriteSource"]
old-location: wic\_wic_codec_iwicbitmapframeencode_writesource.htm
tech.root: wic
ms.assetid: bc748982-6dc8-41cc-a23b-9d127dc22a1f
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],WriteSource method, IWICBitmapFrameEncode.WriteSource, IWICBitmapFrameEncode::WriteSource, WriteSource, WriteSource method [Windows Imaging Component], WriteSource method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_writesource, wic._wic_codec_iwicbitmapframeencode_writesource, wincodec/IWICBitmapFrameEncode::WriteSource
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
 - IWICBitmapFrameEncode::WriteSource
 - wincodec/IWICBitmapFrameEncode::WriteSource
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
 - IWICBitmapFrameEncode.WriteSource
---

# IWICBitmapFrameEncode::WriteSource


## -description

Encodes a bitmap source.

## -parameters

### -param pIBitmapSource [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The bitmap source to encode.

### -param prc [in]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicrect">WICRect</a>*</b>

The size rectangle of the bitmap source.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setsize">SetSize</a> is not called prior to calling <b>WriteSource</b>, the size given in <i>prc</i> is used if not <b>NULL</b>. Otherwise, the size of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> given in <i>pIBitmapSource</i> is used. 

If <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat">SetPixelFormat</a> is not called prior to calling <b>WriteSource</b>, the pixel format of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> given in <i>pIBitmapSource</i> is used.

If <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setresolution">SetResolution</a> is not called prior to calling <b>WriteSource</b>, the pixel format of <i>pIBitmapSource</i> is used.

If <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setpalette">SetPalette</a> is not called prior to calling <b>WriteSource</b>, the target pixel format is indexed, and the pixel format of <i>pIBitmapSource</i> matches the encoder frame's pixel format, then the <i>pIBitmapSource</i> pixel format is used.

When encoding a GIF image, if the global palette is set and the frame level palette is not set directly by the user or by a custom independent software vendor (ISV) GIF codec, <b>WriteSource</b> will use the global palette to encode the frame even when <i>pIBitmapSource</i> has a frame level palette.

Starting with  Windows Vista, repeated <b>WriteSource</b> calls can be made as long as the total accumulated source rect height is the same as set through <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setsize">SetSize</a>.

Starting with Windows 8.1, the source rect must be at least the dimensions set through <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setsize">SetSize</a>. If the source rect width exceeds the <b>SetSize</b> width, extra pixels on the right side are ignored. If the source rect height exceeds the remaining unfilled height, extra scan lines on the bottom are ignored.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>



<a href="/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>