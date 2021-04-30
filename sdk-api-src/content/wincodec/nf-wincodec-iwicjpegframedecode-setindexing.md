---
UID: NF:wincodec.IWICJpegFrameDecode.SetIndexing
title: IWICJpegFrameDecode::SetIndexing (wincodec.h)
description: Enables indexing of the JPEG for efficient random access.
helpviewer_keywords: ["IWICJpegFrameDecode interface [Windows Imaging Component]","SetIndexing method","IWICJpegFrameDecode.SetIndexing","IWICJpegFrameDecode::SetIndexing","SetIndexing","SetIndexing method [Windows Imaging Component]","SetIndexing method [Windows Imaging Component]","IWICJpegFrameDecode interface","wic.iwicjpegframedecode_setindexing","wincodec/IWICJpegFrameDecode::SetIndexing"]
old-location: wic\iwicjpegframedecode_setindexing.htm
tech.root: wic
ms.assetid: D97A48E5-0398-460C-AFA9-2E1B8744926B
ms.date: 12/05/2018
ms.keywords: IWICJpegFrameDecode interface [Windows Imaging Component],SetIndexing method, IWICJpegFrameDecode.SetIndexing, IWICJpegFrameDecode::SetIndexing, SetIndexing, SetIndexing method [Windows Imaging Component], SetIndexing method [Windows Imaging Component],IWICJpegFrameDecode interface, wic.iwicjpegframedecode_setindexing, wincodec/IWICJpegFrameDecode::SetIndexing
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
 - IWICJpegFrameDecode::SetIndexing
 - wincodec/IWICJpegFrameDecode::SetIndexing
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
 - IWICJpegFrameDecode.SetIndexing
---

# IWICJpegFrameDecode::SetIndexing


## -description

Enables indexing of the JPEG for efficient random access.

## -parameters

### -param options

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicjpegindexingoptions">WICJpegIndexingOptions</a></b>

A value specifying whether indexes should be generated immediately or deferred until a future call to <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">IWICBitmapSource::CopyPixels</a>.

### -param horizontalIntervalSize

Type: <b>UINT</b>

The granularity of the indexing, in pixels.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK upon successful completion.

## -remarks

This method enables efficient random-access to the image pixels at the expense of memory usage.  The amount of memory required for indexing depends on the requested index granularity.   Unless <b>SetIndexing</b> is called, it is much more efficient to access a JPEG by progressing through its pixels top-down during calls to <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">IWICBitmapSource::CopyPixels</a>.


This method will fail if indexing is unsupported on the file.  <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-doessupportindexing">IWICJpegFrameDecode::DoesSupportIndexing</a> should be called to first determine whether indexing is supported.  If this method is called multiple times, the final call changes the index granularity to the requested size.


The provided interval size controls horizontal spacing of index entries.  This value is internally rounded up according to the JPEG’s MCU (minimum coded unit) size, which is typically either 8 or 16 unscaled pixels.  The vertical size of the index interval is always equal to one MCU size.

Indexes can be generated immediately, or during future calls to <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">IWICBitmapSource::CopyPixels</a> to reduce redundant decompression work.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">IWICBitmapSource::CopyPixels</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicjpegframedecode">IWICJpegFrameDecode</a>



<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-clearindexing">IWICJpegFrameDecode::ClearIndexing</a>



<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-doessupportindexing">IWICJpegFrameDecode::DoesSupportIndexing</a>