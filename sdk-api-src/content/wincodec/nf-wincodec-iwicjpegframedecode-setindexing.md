---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

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
 

 

