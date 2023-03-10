---
UID: NF:wincodec.IWICBitmapDecoder.GetColorContexts
title: IWICBitmapDecoder::GetColorContexts (wincodec.h)
description: Retrieves the IWICColorContext objects of the image.
helpviewer_keywords: ["GetColorContexts","GetColorContexts method [Windows Imaging Component]","GetColorContexts method [Windows Imaging Component]","IWICBitmapDecoder interface","IWICBitmapDecoder interface [Windows Imaging Component]","GetColorContexts method","IWICBitmapDecoder.GetColorContexts","IWICBitmapDecoder::GetColorContexts","_wic_codec_iwicbitmapdecoder_getcolorcontexts","wic._wic_codec_iwicbitmapdecoder_getcolorcontexts","wincodec/IWICBitmapDecoder::GetColorContexts"]
old-location: wic\_wic_codec_iwicbitmapdecoder_getcolorcontexts.htm
tech.root: wic
ms.assetid: 55fdf9c0-5fa4-46e2-b4d2-42b8d4c90887
ms.date: 12/05/2018
ms.keywords: GetColorContexts, GetColorContexts method [Windows Imaging Component], GetColorContexts method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],GetColorContexts method, IWICBitmapDecoder.GetColorContexts, IWICBitmapDecoder::GetColorContexts, _wic_codec_iwicbitmapdecoder_getcolorcontexts, wic._wic_codec_iwicbitmapdecoder_getcolorcontexts, wincodec/IWICBitmapDecoder::GetColorContexts
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapDecoder::GetColorContexts
 - wincodec/IWICBitmapDecoder::GetColorContexts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICBitmapDecoder.GetColorContexts
---

# IWICBitmapDecoder::GetColorContexts


## -description

Retrieves the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> objects of the image.

## -parameters

### -param cCount [in]

Type: <b>UINT</b>

The number of color contexts to retrieve.

This value must be the size of, or smaller than, the size available to <i>ppIColorContexts</i>.

### -param ppIColorContexts [in, out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>**</b>

A pointer that receives a pointer to the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>.

### -param pcActualCount [out]

Type: <b>UINT*</b>

A pointer that receives the number of color contexts contained in the image.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.