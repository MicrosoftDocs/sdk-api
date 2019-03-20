---
UID: NF:wincodec.IWICBitmapDecoderInfo.MatchesPattern
title: IWICBitmapDecoderInfo::MatchesPattern (wincodec.h)
author: windows-sdk-content
description: Retrieves a value that indicates whether the codec recognizes the pattern within a specified stream.
old-location: wic\_wic_codec_iwicbitmapdecoderinfo_matchespattern.htm
tech.root: wic
ms.assetid: 159459a4-f14e-4441-94a6-d55b3bacb868
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWICBitmapDecoderInfo interface [Windows Imaging Component],MatchesPattern method, IWICBitmapDecoderInfo.MatchesPattern, IWICBitmapDecoderInfo::MatchesPattern, MatchesPattern, MatchesPattern method [Windows Imaging Component], MatchesPattern method [Windows Imaging Component],IWICBitmapDecoderInfo interface, _wic_codec_iwicbitmapdecoderinfo_matchespattern, wic._wic_codec_iwicbitmapdecoderinfo_matchespattern, wincodec/IWICBitmapDecoderInfo::MatchesPattern
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapDecoderInfo.MatchesPattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapDecoderInfo::MatchesPattern


## -description


Retrieves a value that indicates whether the codec recognizes the pattern within a specified stream.


## -parameters




### -param pIStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The stream to pattern match within.


### -param pfMatches [out]

Type: <b>BOOL*</b>

A pointer that receives <b>TRUE</b> if the patterns match; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



