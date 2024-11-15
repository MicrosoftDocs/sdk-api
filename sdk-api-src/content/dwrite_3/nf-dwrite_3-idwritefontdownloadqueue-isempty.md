---
UID: NF:dwrite_3.IDWriteFontDownloadQueue.IsEmpty
title: IDWriteFontDownloadQueue::IsEmpty (dwrite_3.h)
description: Determines whether the download queue is empty. Note that the queue does not include requests that are already being downloaded. Calling BeginDownloadclears the queue.
helpviewer_keywords: ["IDWriteFontDownloadQueue interface [Direct Write]","IsEmpty method","IDWriteFontDownloadQueue.IsEmpty","IDWriteFontDownloadQueue::IsEmpty","IsEmpty","IsEmpty method [Direct Write]","IsEmpty method [Direct Write]","IDWriteFontDownloadQueue interface","directwrite.idwritefontdownloadqueue_isempty","dwrite_3/IDWriteFontDownloadQueue::IsEmpty"]
old-location: directwrite\idwritefontdownloadqueue_isempty.htm
tech.root: DirectWrite
ms.assetid: 2f1f0d1c-0db8-c382-7879-92a889cfeb6b
ms.date: 12/05/2018
ms.keywords: IDWriteFontDownloadQueue interface [Direct Write],IsEmpty method, IDWriteFontDownloadQueue.IsEmpty, IDWriteFontDownloadQueue::IsEmpty, IsEmpty, IsEmpty method [Direct Write], IsEmpty method [Direct Write],IDWriteFontDownloadQueue interface, directwrite.idwritefontdownloadqueue_isempty, dwrite_3/IDWriteFontDownloadQueue::IsEmpty
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
 - IDWriteFontDownloadQueue::IsEmpty
 - dwrite_3/IDWriteFontDownloadQueue::IsEmpty
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
 - IDWriteFontDownloadQueue.IsEmpty
---

# IDWriteFontDownloadQueue::IsEmpty


## -description

Determines whether the download queue is empty. Note that the queue does not    
    include requests that are already being downloaded. Calling <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload">BeginDownload</a> clears the queue.



## -returns

Type: <b>BOOL</b>

TRUE if the queue is empty, FALSE if there are requests pending for <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload">BeginDownload</a>.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>

