---
UID: NF:wincodec.IWICDdsFrameDecode.GetSizeInBlocks
title: IWICDdsFrameDecode::GetSizeInBlocks (wincodec.h)
description: Gets the width and height, in blocks, of the DDS image.
helpviewer_keywords: ["GetSizeInBlocks","GetSizeInBlocks method [Windows Imaging Component]","GetSizeInBlocks method [Windows Imaging Component]","IWICDdsFrameDecode interface","IWICDdsFrameDecode interface [Windows Imaging Component]","GetSizeInBlocks method","IWICDdsFrameDecode.GetSizeInBlocks","IWICDdsFrameDecode::GetSizeInBlocks","wic.iwicddsframedecode_getsizeinblocks","wincodec/IWICDdsFrameDecode::GetSizeInBlocks"]
old-location: wic\iwicddsframedecode_getsizeinblocks.htm
tech.root: wic
ms.assetid: 34F3A19C-4B68-4E6A-AE08-71DE9A0687BF
ms.date: 12/05/2018
ms.keywords: GetSizeInBlocks, GetSizeInBlocks method [Windows Imaging Component], GetSizeInBlocks method [Windows Imaging Component],IWICDdsFrameDecode interface, IWICDdsFrameDecode interface [Windows Imaging Component],GetSizeInBlocks method, IWICDdsFrameDecode.GetSizeInBlocks, IWICDdsFrameDecode::GetSizeInBlocks, wic.iwicddsframedecode_getsizeinblocks, wincodec/IWICDdsFrameDecode::GetSizeInBlocks
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
 - IWICDdsFrameDecode::GetSizeInBlocks
 - wincodec/IWICDdsFrameDecode::GetSizeInBlocks
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
 - IWICDdsFrameDecode.GetSizeInBlocks
---

# IWICDdsFrameDecode::GetSizeInBlocks


## -description

Gets the width and height, in blocks, of the DDS image.

## -parameters

### -param pWidthInBlocks [out]

Type: <b>UINT*</b>

The width of the DDS image in blocks.

### -param pHeightInBlocks [out]

Type: <b>UINT*</b>

The height of the DDS image in blocks.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For block compressed textures, the returned width and height values do not completely define the texture size because the image is padded to fit the closest whole block size. For example, three BC1 textures with pixel dimensions of 1x1, 2x2 and 4x4 will all report <i>pWidthInBlocks</i> = 1 and <i>pHeightInBlocks</i> = 1.



If the texture does not use a block-compressed <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>, this method returns the texture size in pixels; for these formats the block size returned by <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-getformatinfo">IWICDdsFrameDecoder::GetFormatInfo</a> is 1x1.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode">IWICDdsFrameDecode</a>