---
UID: NF:wincodec.IWICDdsDecoder.GetFrame
title: IWICDdsDecoder::GetFrame (wincodec.h)
description: Retrieves the specified frame of the DDS image.
helpviewer_keywords: ["GetFrame","GetFrame method [Windows Imaging Component]","GetFrame method [Windows Imaging Component]","IWICDdsDecoder interface","IWICDdsDecoder interface [Windows Imaging Component]","GetFrame method","IWICDdsDecoder.GetFrame","IWICDdsDecoder::GetFrame","wic.iwicddsdecoder_getframe","wincodec/IWICDdsDecoder::GetFrame"]
old-location: wic\iwicddsdecoder_getframe.htm
tech.root: wic
ms.assetid: 8842FD14-575B-4A81-9598-83A5A67415B7
ms.date: 12/05/2018
ms.keywords: GetFrame, GetFrame method [Windows Imaging Component], GetFrame method [Windows Imaging Component],IWICDdsDecoder interface, IWICDdsDecoder interface [Windows Imaging Component],GetFrame method, IWICDdsDecoder.GetFrame, IWICDdsDecoder::GetFrame, wic.iwicddsdecoder_getframe, wincodec/IWICDdsDecoder::GetFrame
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
 - IWICDdsDecoder::GetFrame
 - wincodec/IWICDdsDecoder::GetFrame
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
 - IWICDdsDecoder.GetFrame
---

# IWICDdsDecoder::GetFrame


## -description

Retrieves the specified frame of the DDS image.

## -parameters

### -param arrayIndex [in]

Type: <b>UINT</b>

The requested index within the texture array.

### -param mipLevel [in]

Type: <b>UINT</b>

The requested mip level.

### -param sliceIndex [in]

Type: <b>UINT</b>

The requested slice within the 3D texture.

### -param ppIBitmapFrame [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a>**</b>

A pointer to a  <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A DDS file can contain multiple images that are organized into a three level hierarchy. First, DDS file may contain multiple textures in a texture array. Second, each texture can have multiple mip levels. Finally, the texture may be a 3D (volume) texture and have multiple slices, each of which is a 2D texture. See the <a href="/windows/desktop/direct3ddds/dx-graphics-dds">DDS documentation</a> for more information.

WIC maps this three level hierarchy into a linear array of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a>, accessible via <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframe">IWICBitmapDecoder::GetFrame</a>. However, determining which frame corresponds to a triad of <i>arrayIndex</i>, <i>mipLevel</i>, and <i>sliceIndex</i> value is not trivial because each mip level of a 3D texture has a different depth (number of slices). This method provides additional convenience over <b>IWICBitmapDecoder::GetFrame</b> for DDS images by calculating the correct frame given the three indices.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createbitmap">CreateBitmap</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder">IWICDdsDecoder</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsformatinfo">WICDdsFormatInfo</a>