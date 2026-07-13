---
UID: NF:wincodec.IWICBitmapFrameEncode.SetResolution
title: IWICBitmapFrameEncode::SetResolution (wincodec.h)
description: Sets the physical resolution of the output image.
helpviewer_keywords: ["IWICBitmapFrameEncode interface [Windows Imaging Component]","SetResolution method","IWICBitmapFrameEncode.SetResolution","IWICBitmapFrameEncode::SetResolution","SetResolution","SetResolution method [Windows Imaging Component]","SetResolution method [Windows Imaging Component]","IWICBitmapFrameEncode interface","_wic_codec_iwicbitmapframeencode_setresolution","wic._wic_codec_iwicbitmapframeencode_setresolution","wincodec/IWICBitmapFrameEncode::SetResolution"]
old-location: wic\_wic_codec_iwicbitmapframeencode_setresolution.htm
tech.root: wic
ms.assetid: 0b9e564a-5278-41d7-84ab-8b7594e776c7
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],SetResolution method, IWICBitmapFrameEncode.SetResolution, IWICBitmapFrameEncode::SetResolution, SetResolution, SetResolution method [Windows Imaging Component], SetResolution method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_setresolution, wic._wic_codec_iwicbitmapframeencode_setresolution, wincodec/IWICBitmapFrameEncode::SetResolution
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
 - IWICBitmapFrameEncode::SetResolution
 - wincodec/IWICBitmapFrameEncode::SetResolution
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
 - IWICBitmapFrameEncode.SetResolution
---

# IWICBitmapFrameEncode::SetResolution


## -description

Sets the physical resolution of the output image.

## -parameters

### -param dpiX [in]

Type: <b>double</b>

The horizontal resolution value.

### -param dpiY [in]

Type: <b>double</b>

The vertical resolution value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Windows Imaging Component (WIC) doesn't perform any special processing as a result of DPI resolution values. For example, data returned from <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">IWICBitmapSource::CopyPixels</a> isn't scaled by the DPI. The app must handle DPI resolution.