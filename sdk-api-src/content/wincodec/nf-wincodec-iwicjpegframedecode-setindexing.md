---
UID: NF:wincodec.IWICJpegFrameDecode.SetIndexing
title: IWICJpegFrameDecode::SetIndexing (wincodec.h)
author: windows-sdk-content
description: Enables indexing of the JPEG for efficient random access.
old-location: wic\iwicjpegframedecode_setindexing.htm
tech.root: wic
ms.assetid: D97A48E5-0398-460C-AFA9-2E1B8744926B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICJpegFrameDecode interface [Windows Imaging Component],SetIndexing method, IWICJpegFrameDecode.SetIndexing, IWICJpegFrameDecode::SetIndexing, SetIndexing, SetIndexing method [Windows Imaging Component], SetIndexing method [Windows Imaging Component],IWICJpegFrameDecode interface, wic.iwicjpegframedecode_setindexing, wincodec/IWICJpegFrameDecode::SetIndexing
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
 - IWICJpegFrameDecode.SetIndexing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICJpegFrameDecode::SetIndexing


## -description


Enables indexing of the JPEG for efficient random access.


## -parameters




### -param options

Type: <b><a href="https://msdn.microsoft.com/AFA9CC1B-847A-4237-9942-EC721FA86E4E">WICJpegIndexingOptions</a></b>

A value specifying whether indexes should be generated immediately or deferred until a future call to <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">IWICBitmapSource::CopyPixels</a>.


### -param horizontalIntervalSize

Type: <b>UINT</b>

The granularity of the indexing, in pixels.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK upon successful completion.




## -remarks



This method enables efficient random-access to the image pixels at the expense of memory usage.  The amount of memory required for indexing depends on the requested index granularity.   Unless <b>SetIndexing</b> is called, it is much more efficient to access a JPEG by progressing through its pixels top-down during calls to <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">IWICBitmapSource::CopyPixels</a>.


This method will fail if indexing is unsupported on the file.  <a href="https://msdn.microsoft.com/99486168-6BF9-40C2-B9D8-903A73AAD125">IWICJpegFrameDecode::DoesSupportIndexing</a> should be called to first determine whether indexing is supported.  If this method is called multiple times, the final call changes the index granularity to the requested size.


The provided interval size controls horizontal spacing of index entries.  This value is internally rounded up according to the JPEG’s MCU (minimum coded unit) size, which is typically either 8 or 16 unscaled pixels.  The vertical size of the index interval is always equal to one MCU size.

Indexes can be generated immediately, or during future calls to <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">IWICBitmapSource::CopyPixels</a> to reduce redundant decompression work. 




## -see-also




<a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">IWICBitmapSource::CopyPixels</a>



<a href="https://msdn.microsoft.com/E6310320-53A8-40F1-8964-D21D8054E1B8">IWICJpegFrameDecode</a>



<a href="https://msdn.microsoft.com/467E0100-F00B-4D2D-BF2A-8138765C787E">IWICJpegFrameDecode::ClearIndexing</a>



<a href="https://msdn.microsoft.com/99486168-6BF9-40C2-B9D8-903A73AAD125">IWICJpegFrameDecode::DoesSupportIndexing</a>
 

 

