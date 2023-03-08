---
UID: NF:wincodec.IWICDdsFrameDecode.CopyBlocks
title: IWICDdsFrameDecode::CopyBlocks (wincodec.h)
description: Requests pixel data as it is natively stored within the DDS file.
helpviewer_keywords: ["CopyBlocks","CopyBlocks method [Windows Imaging Component]","CopyBlocks method [Windows Imaging Component]","IWICDdsFrameDecode interface","IWICDdsFrameDecode interface [Windows Imaging Component]","CopyBlocks method","IWICDdsFrameDecode.CopyBlocks","IWICDdsFrameDecode::CopyBlocks","wic.iwicddsframedecode_copyblocks","wincodec/IWICDdsFrameDecode::CopyBlocks"]
old-location: wic\iwicddsframedecode_copyblocks.htm
tech.root: wic
ms.assetid: D090AA8E-46F2-40C9-A156-12038053E040
ms.date: 12/05/2018
ms.keywords: CopyBlocks, CopyBlocks method [Windows Imaging Component], CopyBlocks method [Windows Imaging Component],IWICDdsFrameDecode interface, IWICDdsFrameDecode interface [Windows Imaging Component],CopyBlocks method, IWICDdsFrameDecode.CopyBlocks, IWICDdsFrameDecode::CopyBlocks, wic.iwicddsframedecode_copyblocks, wincodec/IWICDdsFrameDecode::CopyBlocks
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IWICDdsFrameDecode::CopyBlocks
 - wincodec/IWICDdsFrameDecode::CopyBlocks
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
 - IWICDdsFrameDecode.CopyBlocks
---

# IWICDdsFrameDecode::CopyBlocks


## -description

Requests pixel data as it is natively stored within the DDS file.

## -parameters

### -param prcBoundsInBlocks [in]

Type: <b>const <a href="/windows/desktop/api/wincodec/ns-wincodec-wicrect">WICRect</a>*</b>

The rectangle to copy from the source. A NULL value specifies the entire texture.

If the texture uses a block-compressed <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>, all values of the rectangle are expressed in number of blocks, not pixels.

### -param cbStride [in]

Type: <b>UINT</b>

The stride, in bytes, of the destination buffer. This represents the number of bytes from the buffer pointer to the next row of data. If the texture uses a block-compressed <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>, a "row of data" is defined as a row of blocks which contains multiple pixel scanlines.

### -param cbBufferSize [in]

Type: <b>UINT</b>

The size, in bytes, of the destination buffer.

### -param pbBuffer [out]

Type: <b>BYTE*</b>

A pointer to the destination buffer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the texture does not use a block-compressed <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>, this method behaves similarly to <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">IWICBitmapSource::CopyPixels</a>. However, it does not perform any pixel format conversion, and instead produces the raw data from the DDS file.

If the texture uses a block-compressed <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>, this method copies the block data directly into the provided buffer. In this case, the <i>prcBoundsInBlocks</i> parameter is defined in blocks, not pixels. To determine if this is the case, call <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-getformatinfo">GetFormatInfo</a> and read the <b>DxgiFormat</b> member of the returned <a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsformatinfo">WICDdsFormatInfo</a> structure.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">IWICBitmapSource::CopyPixels</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode">IWICDdsFrameDecode</a>