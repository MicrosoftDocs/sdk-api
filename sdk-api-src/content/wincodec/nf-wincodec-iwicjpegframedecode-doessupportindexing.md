---
UID: NF:wincodec.IWICJpegFrameDecode.DoesSupportIndexing
title: IWICJpegFrameDecode::DoesSupportIndexing (wincodec.h)
description: Retrieves a value indicating whether this decoder supports indexing for efficient random access.
helpviewer_keywords: ["DoesSupportIndexing","DoesSupportIndexing method [Windows Imaging Component]","DoesSupportIndexing method [Windows Imaging Component]","IWICJpegFrameDecode interface","IWICJpegFrameDecode interface [Windows Imaging Component]","DoesSupportIndexing method","IWICJpegFrameDecode.DoesSupportIndexing","IWICJpegFrameDecode::DoesSupportIndexing","wic.iwicjpegframedecode_doessupportindexing","wincodec/IWICJpegFrameDecode::DoesSupportIndexing"]
old-location: wic\iwicjpegframedecode_doessupportindexing.htm
tech.root: wic
ms.assetid: 99486168-6BF9-40C2-B9D8-903A73AAD125
ms.date: 12/05/2018
ms.keywords: DoesSupportIndexing, DoesSupportIndexing method [Windows Imaging Component], DoesSupportIndexing method [Windows Imaging Component],IWICJpegFrameDecode interface, IWICJpegFrameDecode interface [Windows Imaging Component],DoesSupportIndexing method, IWICJpegFrameDecode.DoesSupportIndexing, IWICJpegFrameDecode::DoesSupportIndexing, wic.iwicjpegframedecode_doessupportindexing, wincodec/IWICJpegFrameDecode::DoesSupportIndexing
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IWICJpegFrameDecode::DoesSupportIndexing
 - wincodec/IWICJpegFrameDecode::DoesSupportIndexing
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
 - IWICJpegFrameDecode.DoesSupportIndexing
---

# IWICJpegFrameDecode::DoesSupportIndexing


## -description

Retrieves a value indicating whether this decoder supports indexing for efficient random access.

## -parameters

### -param pfIndexingSupported

Type: <b>BOOL*</b>

True if indexing is supported; otherwise, false.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on successful completion.

## -remarks

Indexing is only supported for some JPEG types. Call this method

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicjpegframedecode">IWICJpegFrameDecode</a>