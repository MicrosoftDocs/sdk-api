---
UID: NF:wincodec.IWICBitmapDecoderInfo.MatchesPattern
title: IWICBitmapDecoderInfo::MatchesPattern (wincodec.h)
description: Retrieves a value that indicates whether the codec recognizes the pattern within a specified stream.
helpviewer_keywords: ["IWICBitmapDecoderInfo interface [Windows Imaging Component]","MatchesPattern method","IWICBitmapDecoderInfo.MatchesPattern","IWICBitmapDecoderInfo::MatchesPattern","MatchesPattern","MatchesPattern method [Windows Imaging Component]","MatchesPattern method [Windows Imaging Component]","IWICBitmapDecoderInfo interface","_wic_codec_iwicbitmapdecoderinfo_matchespattern","wic._wic_codec_iwicbitmapdecoderinfo_matchespattern","wincodec/IWICBitmapDecoderInfo::MatchesPattern"]
old-location: wic\_wic_codec_iwicbitmapdecoderinfo_matchespattern.htm
tech.root: wic
ms.assetid: 159459a4-f14e-4441-94a6-d55b3bacb868
ms.date: 12/05/2018
ms.keywords: IWICBitmapDecoderInfo interface [Windows Imaging Component],MatchesPattern method, IWICBitmapDecoderInfo.MatchesPattern, IWICBitmapDecoderInfo::MatchesPattern, MatchesPattern, MatchesPattern method [Windows Imaging Component], MatchesPattern method [Windows Imaging Component],IWICBitmapDecoderInfo interface, _wic_codec_iwicbitmapdecoderinfo_matchespattern, wic._wic_codec_iwicbitmapdecoderinfo_matchespattern, wincodec/IWICBitmapDecoderInfo::MatchesPattern
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
 - IWICBitmapDecoderInfo::MatchesPattern
 - wincodec/IWICBitmapDecoderInfo::MatchesPattern
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
 - IWICBitmapDecoderInfo.MatchesPattern
---

# IWICBitmapDecoderInfo::MatchesPattern


## -description

Retrieves a value that indicates whether the codec recognizes the pattern within a specified stream.

## -parameters

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The stream to pattern match within.

### -param pfMatches [out]

Type: <b>BOOL*</b>

A pointer that receives <b>TRUE</b> if the patterns match; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.