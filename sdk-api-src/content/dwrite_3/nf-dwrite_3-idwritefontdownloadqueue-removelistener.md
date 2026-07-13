---
UID: NF:dwrite_3.IDWriteFontDownloadQueue.RemoveListener
title: IDWriteFontDownloadQueue::RemoveListener (dwrite_3.h)
description: Unregisters a notification handler that was previously registered using AddListener.
helpviewer_keywords: ["IDWriteFontDownloadQueue interface [Direct Write]","RemoveListener method","IDWriteFontDownloadQueue.RemoveListener","IDWriteFontDownloadQueue::RemoveListener","RemoveListener","RemoveListener method [Direct Write]","RemoveListener method [Direct Write]","IDWriteFontDownloadQueue interface","directwrite.idwritefontdownloadqueue_removelistener","dwrite_3/IDWriteFontDownloadQueue::RemoveListener"]
old-location: directwrite\idwritefontdownloadqueue_removelistener.htm
tech.root: DirectWrite
ms.assetid: e3470f17-9630-de53-d1ae-ab2a2508a069
ms.date: 09/10/2025
ms.keywords: IDWriteFontDownloadQueue interface [Direct Write],RemoveListener method, IDWriteFontDownloadQueue.RemoveListener, IDWriteFontDownloadQueue::RemoveListener, RemoveListener, RemoveListener method [Direct Write], RemoveListener method [Direct Write],IDWriteFontDownloadQueue interface, directwrite.idwritefontdownloadqueue_removelistener, dwrite_3/IDWriteFontDownloadQueue::RemoveListener
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
 - IDWriteFontDownloadQueue::RemoveListener
 - dwrite_3/IDWriteFontDownloadQueue::RemoveListener
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
 - IDWriteFontDownloadQueue.RemoveListener
---

# IDWriteFontDownloadQueue::RemoveListener


## -description

Unregisters a notification handler that was previously registered using <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-addlistener">AddListener</a>.

## -parameters

### -param token

Type: <b>UINT32</b>

Token value previously returned by <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-addlistener">AddListener</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>

