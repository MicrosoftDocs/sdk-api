---
UID: NF:wincodec.IWICDdsFrameDecode.GetFormatInfo
title: IWICDdsFrameDecode::GetFormatInfo (wincodec.h)
description: Gets information about the format in which the DDS image is stored.
helpviewer_keywords: ["GetFormatInfo","GetFormatInfo method [Windows Imaging Component]","GetFormatInfo method [Windows Imaging Component]","IWICDdsFrameDecode interface","IWICDdsFrameDecode interface [Windows Imaging Component]","GetFormatInfo method","IWICDdsFrameDecode.GetFormatInfo","IWICDdsFrameDecode::GetFormatInfo","wic.iwicddsframedecode_getformatinfo","wincodec/IWICDdsFrameDecode::GetFormatInfo"]
old-location: wic\iwicddsframedecode_getformatinfo.htm
tech.root: wic
ms.assetid: 0D5B9E45-E1EA-4D16-B793-63FEAB2BAF65
ms.date: 12/05/2018
ms.keywords: GetFormatInfo, GetFormatInfo method [Windows Imaging Component], GetFormatInfo method [Windows Imaging Component],IWICDdsFrameDecode interface, IWICDdsFrameDecode interface [Windows Imaging Component],GetFormatInfo method, IWICDdsFrameDecode.GetFormatInfo, IWICDdsFrameDecode::GetFormatInfo, wic.iwicddsframedecode_getformatinfo, wincodec/IWICDdsFrameDecode::GetFormatInfo
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
 - IWICDdsFrameDecode::GetFormatInfo
 - wincodec/IWICDdsFrameDecode::GetFormatInfo
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
 - IWICDdsFrameDecode.GetFormatInfo
---

# IWICDdsFrameDecode::GetFormatInfo


## -description

Gets information about the format in which the DDS image is stored.

## -parameters

### -param pFormatInfo [out]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsformatinfo">WICDdsFormatInfo</a>*</b>

Information about the DDS format.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This information can be used for allocating memory or constructing Direct3D or Direct2D resources, for example by using <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> or <a href="/windows/desktop/Direct2D/id2d1devicecontext-createbitmap-overload">ID2D1DeviceContext::CreateBitmap</a>.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createbitmap">CreateBitmap</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode">IWICDdsFrameDecode</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsformatinfo">WICDdsFormatInfo</a>