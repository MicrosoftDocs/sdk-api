---
UID: NF:wincodec.IWICJpegFrameDecode.DoesSupportIndexing
title: IWICJpegFrameDecode::DoesSupportIndexing (wincodec.h)
author: windows-sdk-content
description: Retrieves a value indicating whether this decoder supports indexing for efficient random access.
old-location: wic\iwicjpegframedecode_doessupportindexing.htm
tech.root: wic
ms.assetid: 99486168-6BF9-40C2-B9D8-903A73AAD125
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DoesSupportIndexing, DoesSupportIndexing method [Windows Imaging Component], DoesSupportIndexing method [Windows Imaging Component],IWICJpegFrameDecode interface, IWICJpegFrameDecode interface [Windows Imaging Component],DoesSupportIndexing method, IWICJpegFrameDecode.DoesSupportIndexing, IWICJpegFrameDecode::DoesSupportIndexing, wic.iwicjpegframedecode_doessupportindexing, wincodec/IWICJpegFrameDecode::DoesSupportIndexing
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICJpegFrameDecode.DoesSupportIndexing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICJpegFrameDecode::DoesSupportIndexing


## -description


Retrieves a value indicating whether this decoder supports indexing for efficient random access.


## -parameters




### -param pfIndexingSupported

Type: <b>BOOL*</b>

True if indexing is supported; otherwise, false.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK on successful completion.




## -remarks



Indexing is only supported for some JPEG types. Call this method




## -see-also




<a href="https://msdn.microsoft.com/E6310320-53A8-40F1-8964-D21D8054E1B8">IWICJpegFrameDecode</a>
 

 

