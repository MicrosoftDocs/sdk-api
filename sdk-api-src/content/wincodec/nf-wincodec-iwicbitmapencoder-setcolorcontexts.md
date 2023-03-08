---
UID: NF:wincodec.IWICBitmapEncoder.SetColorContexts
title: IWICBitmapEncoder::SetColorContexts (wincodec.h)
description: Sets the IWICColorContext objects for the encoder.
helpviewer_keywords: ["IWICBitmapEncoder interface [Windows Imaging Component]","SetColorContexts method","IWICBitmapEncoder.SetColorContexts","IWICBitmapEncoder::SetColorContexts","SetColorContexts","SetColorContexts method [Windows Imaging Component]","SetColorContexts method [Windows Imaging Component]","IWICBitmapEncoder interface","_wic_codec_iwicbitmapencoder_setcolorcontexts","wic._wic_codec_iwicbitmapencoder_setcolorcontexts","wincodec/IWICBitmapEncoder::SetColorContexts"]
old-location: wic\_wic_codec_iwicbitmapencoder_setcolorcontexts.htm
tech.root: wic
ms.assetid: 68e64db9-ee6a-4dc3-bf74-34274211e2dc
ms.date: 12/05/2018
ms.keywords: IWICBitmapEncoder interface [Windows Imaging Component],SetColorContexts method, IWICBitmapEncoder.SetColorContexts, IWICBitmapEncoder::SetColorContexts, SetColorContexts, SetColorContexts method [Windows Imaging Component], SetColorContexts method [Windows Imaging Component],IWICBitmapEncoder interface, _wic_codec_iwicbitmapencoder_setcolorcontexts, wic._wic_codec_iwicbitmapencoder_setcolorcontexts, wincodec/IWICBitmapEncoder::SetColorContexts
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
 - IWICBitmapEncoder::SetColorContexts
 - wincodec/IWICBitmapEncoder::SetColorContexts
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
 - IWICBitmapEncoder.SetColorContexts
---

# IWICBitmapEncoder::SetColorContexts


## -description

Sets the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> objects for the encoder.

## -parameters

### -param cCount [in]

Type: <b>UINT</b>

The number of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> to set.

### -param ppIColorContext [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>**</b>

A pointer an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> pointer containing the color contexts to set for the encoder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.