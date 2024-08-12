---
UID: NF:dwrite_3.IDWriteFontDownloadQueue.AddListener
title: IDWriteFontDownloadQueue::AddListener (dwrite_3.h)
description: Registers a client-defined listener object that receives download notifications. All registered listener's DownloadCompleted will be called after BeginDownloadcompletes.
helpviewer_keywords: ["AddListener","AddListener method [Direct Write]","AddListener method [Direct Write]","IDWriteFontDownloadQueue interface","IDWriteFontDownloadQueue interface [Direct Write]","AddListener method","IDWriteFontDownloadQueue.AddListener","IDWriteFontDownloadQueue::AddListener","directwrite.idwritefontdownloadqueue_addlistener","dwrite_3/IDWriteFontDownloadQueue::AddListener"]
old-location: directwrite\idwritefontdownloadqueue_addlistener.htm
tech.root: DirectWrite
ms.assetid: c539be2d-bc77-cc8a-c78c-226a67b8dd26
ms.date: 12/05/2018
ms.keywords: AddListener, AddListener method [Direct Write], AddListener method [Direct Write],IDWriteFontDownloadQueue interface, IDWriteFontDownloadQueue interface [Direct Write],AddListener method, IDWriteFontDownloadQueue.AddListener, IDWriteFontDownloadQueue::AddListener, directwrite.idwritefontdownloadqueue_addlistener, dwrite_3/IDWriteFontDownloadQueue::AddListener
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
 - IDWriteFontDownloadQueue::AddListener
 - dwrite_3/IDWriteFontDownloadQueue::AddListener
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
 - IDWriteFontDownloadQueue.AddListener
---

# IDWriteFontDownloadQueue::AddListener


## -description

Registers a client-defined listener object that receives download notifications.  
    All registered listener's DownloadCompleted will be called after <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload">BeginDownload</a> completes.

## -parameters

### -param listener

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener">IDWriteFontDownloadListener</a>*</b>

Listener object to add.

### -param token [out]

Type: <b>UINT32*</b>

Receives a token value, which the caller must subsequently pass to <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-removelistener">RemoveListener</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener">IDWriteFontDownloadListener</a> can also be passed to <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload">BeginDownload</a> 
      using the context parameter, rather than globally registered to the queue.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>

