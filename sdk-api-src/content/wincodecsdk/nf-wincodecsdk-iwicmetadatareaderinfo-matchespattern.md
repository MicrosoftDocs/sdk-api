---
UID: NF:wincodecsdk.IWICMetadataReaderInfo.MatchesPattern
title: IWICMetadataReaderInfo::MatchesPattern (wincodecsdk.h)
description: Determines if a stream contains a metadata item pattern.
helpviewer_keywords: ["IWICMetadataReaderInfo interface [Windows Imaging Component]","MatchesPattern method","IWICMetadataReaderInfo.MatchesPattern","IWICMetadataReaderInfo::MatchesPattern","MatchesPattern","MatchesPattern method [Windows Imaging Component]","MatchesPattern method [Windows Imaging Component]","IWICMetadataReaderInfo interface","_wic_codec_iwicmetadatareaderinfo_matchespattern","wic._wic_codec_iwicmetadatareaderinfo_matchespattern","wincodecsdk/IWICMetadataReaderInfo::MatchesPattern"]
old-location: wic\_wic_codec_iwicmetadatareaderinfo_matchespattern.htm
tech.root: wic
ms.assetid: 58ac58f4-25e0-4fc4-8d2a-854bb89e4af6
ms.date: 12/05/2018
ms.keywords: IWICMetadataReaderInfo interface [Windows Imaging Component],MatchesPattern method, IWICMetadataReaderInfo.MatchesPattern, IWICMetadataReaderInfo::MatchesPattern, MatchesPattern, MatchesPattern method [Windows Imaging Component], MatchesPattern method [Windows Imaging Component],IWICMetadataReaderInfo interface, _wic_codec_iwicmetadatareaderinfo_matchespattern, wic._wic_codec_iwicmetadatareaderinfo_matchespattern, wincodecsdk/IWICMetadataReaderInfo::MatchesPattern
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
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
 - IWICMetadataReaderInfo::MatchesPattern
 - wincodecsdk/IWICMetadataReaderInfo::MatchesPattern
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
 - IWICMetadataReaderInfo.MatchesPattern
---

# IWICMetadataReaderInfo::MatchesPattern


## -description

Determines if a stream contains a metadata item pattern.

## -parameters

### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The container format of the metadata item.

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The stream to search for the metadata pattern.

### -param pfMatches [out]

Type: <b>BOOL*</b>

Pointer that receives <code>TRUE</code> if the stream contains the pattern; otherwise, <code>FALSE</code>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.