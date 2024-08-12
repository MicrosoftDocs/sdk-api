---
UID: NF:dwrite_3.IDWriteFontDownloadQueue.GetGenerationCount
title: IDWriteFontDownloadQueue::GetGenerationCount (dwrite_3.h)
description: Gets the current generation number of the download queue, which is incremented every time after a download completes, whether failed or successful. This cookie value can be compared against cached data to determine if it is stale.
helpviewer_keywords: ["GetGenerationCount","GetGenerationCount method [Direct Write]","GetGenerationCount method [Direct Write]","IDWriteFontDownloadQueue interface","IDWriteFontDownloadQueue interface [Direct Write]","GetGenerationCount method","IDWriteFontDownloadQueue.GetGenerationCount","IDWriteFontDownloadQueue::GetGenerationCount","directwrite.idwritefontdownloadqueue_getgenerationcount","dwrite_3/IDWriteFontDownloadQueue::GetGenerationCount"]
old-location: directwrite\idwritefontdownloadqueue_getgenerationcount.htm
tech.root: DirectWrite
ms.assetid: 6fbbe575-b186-7ffb-ff32-efceccccc48c
ms.date: 12/05/2018
ms.keywords: GetGenerationCount, GetGenerationCount method [Direct Write], GetGenerationCount method [Direct Write],IDWriteFontDownloadQueue interface, IDWriteFontDownloadQueue interface [Direct Write],GetGenerationCount method, IDWriteFontDownloadQueue.GetGenerationCount, IDWriteFontDownloadQueue::GetGenerationCount, directwrite.idwritefontdownloadqueue_getgenerationcount, dwrite_3/IDWriteFontDownloadQueue::GetGenerationCount
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
 - IDWriteFontDownloadQueue::GetGenerationCount
 - dwrite_3/IDWriteFontDownloadQueue::GetGenerationCount
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
 - IDWriteFontDownloadQueue.GetGenerationCount
---

# IDWriteFontDownloadQueue::GetGenerationCount


## -description

Gets the current generation number of the download queue, which is incremented   
    every time after a download completes, whether failed or successful. This cookie  
    value can be compared against cached data to determine if it is stale.



## -returns

Type: <b>UINT64</b>

The current generation number of the download queue.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>

