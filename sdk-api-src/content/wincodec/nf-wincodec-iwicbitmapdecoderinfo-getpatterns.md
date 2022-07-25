---
UID: NF:wincodec.IWICBitmapDecoderInfo.GetPatterns
title: IWICBitmapDecoderInfo::GetPatterns (wincodec.h)
description: Retrieves the file pattern signatures supported by the decoder.
helpviewer_keywords: ["GetPatterns","GetPatterns method [Windows Imaging Component]","GetPatterns method [Windows Imaging Component]","IWICBitmapDecoderInfo interface","IWICBitmapDecoderInfo interface [Windows Imaging Component]","GetPatterns method","IWICBitmapDecoderInfo.GetPatterns","IWICBitmapDecoderInfo::GetPatterns","_wic_codec_iwicbitmapdecoderinfo_getpatterns","wic._wic_codec_iwicbitmapdecoderinfo_getpatterns","wincodec/IWICBitmapDecoderInfo::GetPatterns"]
old-location: wic\_wic_codec_iwicbitmapdecoderinfo_getpatterns.htm
tech.root: wic
ms.assetid: 6143a431-cea6-4ced-adf5-2aa4d90d622f
ms.date: 12/05/2018
ms.keywords: GetPatterns, GetPatterns method [Windows Imaging Component], GetPatterns method [Windows Imaging Component],IWICBitmapDecoderInfo interface, IWICBitmapDecoderInfo interface [Windows Imaging Component],GetPatterns method, IWICBitmapDecoderInfo.GetPatterns, IWICBitmapDecoderInfo::GetPatterns, _wic_codec_iwicbitmapdecoderinfo_getpatterns, wic._wic_codec_iwicbitmapdecoderinfo_getpatterns, wincodec/IWICBitmapDecoderInfo::GetPatterns
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
 - IWICBitmapDecoderInfo::GetPatterns
 - wincodec/IWICBitmapDecoderInfo::GetPatterns
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
 - IWICBitmapDecoderInfo.GetPatterns
---

# IWICBitmapDecoderInfo::GetPatterns


## -description

Retrieves the file pattern signatures supported by the decoder.

## -parameters

### -param cbSizePatterns [in]

Type: <b>UINT</b>

The array size of the <i>pPatterns</i> array.

### -param pPatterns [out]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicbitmappattern">WICBitmapPattern</a>*</b>

Receives a list of <a href="/windows/desktop/api/wincodec/ns-wincodec-wicbitmappattern">WICBitmapPattern</a> objects supported by the decoder.

### -param pcPatterns [out]

Type: <b>UINT*</b>

Receives the number of patterns the decoder supports.

### -param pcbPatternsActual [out]

Type: <b>UINT*</b>

Receives the actual buffer size needed to retrieve all pattern signatures supported by the decoder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To retrieve all pattern signatures, this method should first be called with <i>pPatterns</i> set to <code>NULL</code> to retrieve the actual buffer size needed through <i>pcbPatternsActual</i>.
               Once the needed buffer size is known, allocate a buffer of the needed size and call <b>GetPatterns</b> again with the allocated buffer.