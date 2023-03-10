---
UID: NF:wincodec.IWICBitmapFrameEncode.Initialize
title: IWICBitmapFrameEncode::Initialize (wincodec.h)
description: Initializes the frame encoder using the given properties.
helpviewer_keywords: ["IWICBitmapFrameEncode interface [Windows Imaging Component]","Initialize method","IWICBitmapFrameEncode.Initialize","IWICBitmapFrameEncode::Initialize","Initialize","Initialize method [Windows Imaging Component]","Initialize method [Windows Imaging Component]","IWICBitmapFrameEncode interface","_wic_codec_iwicbitmapframeencode_initialize","wic._wic_codec_iwicbitmapframeencode_initialize","wincodec/IWICBitmapFrameEncode::Initialize"]
old-location: wic\_wic_codec_iwicbitmapframeencode_initialize.htm
tech.root: wic
ms.assetid: ec215e32-b4bd-469a-903d-f5b546185183
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],Initialize method, IWICBitmapFrameEncode.Initialize, IWICBitmapFrameEncode::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_initialize, wic._wic_codec_iwicbitmapframeencode_initialize, wincodec/IWICBitmapFrameEncode::Initialize
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
 - IWICBitmapFrameEncode::Initialize
 - wincodec/IWICBitmapFrameEncode::Initialize
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
 - IWICBitmapFrameEncode.Initialize
---

# IWICBitmapFrameEncode::Initialize


## -description

Initializes the frame encoder using the given properties.

## -parameters

### -param pIEncoderOptions [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a>*</b>

The set of properties to use for <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a> initialization.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you don't want any encoding options, pass <b>NULL</b> for <i>pIEncoderOptions</i>. Otherwise, pass the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a> that was provided by <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapencoder-createnewframe">IWICBitmapEncoder::CreateNewFrame</a> with updated values.


For a complete list of encoding options supported by the Windows-provided codecs, see <a href="/windows/desktop/wic/native-wic-codecs">Native WIC Codecs</a>.