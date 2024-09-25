---
UID: NF:dwrite_3.IDWriteFontDownloadQueue.BeginDownload
title: IDWriteFontDownloadQueue::BeginDownload (dwrite_3.h)
description: Begins an asynchronous download operation. The download operation executes in the background until it completes or is cancelled by a CancelDownload call.
helpviewer_keywords: ["BeginDownload","BeginDownload method [Direct Write]","BeginDownload method [Direct Write]","IDWriteFontDownloadQueue interface","IDWriteFontDownloadQueue interface [Direct Write]","BeginDownload method","IDWriteFontDownloadQueue.BeginDownload","IDWriteFontDownloadQueue::BeginDownload","directwrite.idwritefontdownloadqueue_begindownload","dwrite_3/IDWriteFontDownloadQueue::BeginDownload"]
old-location: directwrite\idwritefontdownloadqueue_begindownload.htm
tech.root: DirectWrite
ms.assetid: 1e3b200c-0190-f600-1cb6-4e2a46f882b4
ms.date: 12/05/2018
ms.keywords: BeginDownload, BeginDownload method [Direct Write], BeginDownload method [Direct Write],IDWriteFontDownloadQueue interface, IDWriteFontDownloadQueue interface [Direct Write],BeginDownload method, IDWriteFontDownloadQueue.BeginDownload, IDWriteFontDownloadQueue::BeginDownload, directwrite.idwritefontdownloadqueue_begindownload, dwrite_3/IDWriteFontDownloadQueue::BeginDownload
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontDownloadQueue::BeginDownload
 - dwrite_3/IDWriteFontDownloadQueue::BeginDownload
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontDownloadQueue.BeginDownload
---

# IDWriteFontDownloadQueue::BeginDownload


## -description

Begins an asynchronous download operation. The download operation executes   
    in the background until it completes or is cancelled by a <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-canceldownload">CancelDownload</a> call.

## -parameters

### -param context [in, optional]

Type: <b>IUnknown*</b>

Optional context object that is passed back to the     
          download notification handler's DownloadCompleted method. If the context object  
          implements IDWriteFontDownloadListener, its DownloadCompleted will be called    
          when done.

## -returns

Type: <b>HRESULT</b>

 Returns S_OK if a download was successfully begun, S_FALSE if the queue was 
          empty, or a standard HRESULT error code.

## -remarks

BeginDownload removes all download requests from the queue, transferring them   
      to a background download operation. If any previous downloads are still ongoing     
      when BeginDownload is called again, the new download does not complete until     
      the previous downloads have finished.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>

