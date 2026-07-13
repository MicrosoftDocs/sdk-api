---
UID: NF:wincodec.IWICBitmapFrameDecode.GetColorContexts
title: IWICBitmapFrameDecode::GetColorContexts (wincodec.h)
description: Retrieves the IWICColorContext associated with the image frame.
helpviewer_keywords: ["GetColorContexts","GetColorContexts method [Windows Imaging Component]","GetColorContexts method [Windows Imaging Component]","IWICBitmapFrameDecode interface","IWICBitmapFrameDecode interface [Windows Imaging Component]","GetColorContexts method","IWICBitmapFrameDecode.GetColorContexts","IWICBitmapFrameDecode::GetColorContexts","_wic_codec_iwicbitmapframedecode_getcolorcontexts","wic._wic_codec_iwicbitmapframedecode_getcolorcontexts","wincodec/IWICBitmapFrameDecode::GetColorContexts"]
old-location: wic\_wic_codec_iwicbitmapframedecode_getcolorcontexts.htm
tech.root: wic
ms.assetid: b869fc51-0f03-4f93-b5ad-805f9b216423
ms.date: 12/05/2018
ms.keywords: GetColorContexts, GetColorContexts method [Windows Imaging Component], GetColorContexts method [Windows Imaging Component],IWICBitmapFrameDecode interface, IWICBitmapFrameDecode interface [Windows Imaging Component],GetColorContexts method, IWICBitmapFrameDecode.GetColorContexts, IWICBitmapFrameDecode::GetColorContexts, _wic_codec_iwicbitmapframedecode_getcolorcontexts, wic._wic_codec_iwicbitmapframedecode_getcolorcontexts, wincodec/IWICBitmapFrameDecode::GetColorContexts
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
 - IWICBitmapFrameDecode::GetColorContexts
 - wincodec/IWICBitmapFrameDecode::GetColorContexts
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
 - IWICBitmapFrameDecode.GetColorContexts
---

# IWICBitmapFrameDecode::GetColorContexts


## -description

Retrieves the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> associated with the image frame.

## -parameters

### -param cCount [in]

Type: <b>UINT</b>

The number of color contexts to retrieve.

This value must be the size of, or smaller than, the size available to <i>ppIColorContexts</i>.

### -param ppIColorContexts [in, out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>**</b>

A pointer that receives a pointer to the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> objects.

### -param pcActualCount [out]

Type: <b>UINT*</b>

A pointer that receives the number of color contexts contained in the image frame.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If NULL is passed for <i>ppIColorContexts</i>, and 0 is passed for <i>cCount</i>, this method will return the total number of color contexts in the image in <i>pcActualCount</i>.



The <i>ppIColorContexts</i> array must be filled with valid data: each <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext*</a> in the array must have been created using <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createcolorcontext">IWICImagingFactory::CreateColorContext</a>.