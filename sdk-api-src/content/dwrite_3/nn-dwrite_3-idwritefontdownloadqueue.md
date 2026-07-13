---
UID: NN:dwrite_3.IDWriteFontDownloadQueue
title: IDWriteFontDownloadQueue (dwrite_3.h)
description: Interface that enqueues download requests for remote fonts, characters, glyphs, and font fragments.
helpviewer_keywords: ["IDWriteFontDownloadQueue","IDWriteFontDownloadQueue interface [Direct Write]","IDWriteFontDownloadQueue interface [Direct Write]","described","directwrite.idwritefontdownloadqueue","dwrite_3/IDWriteFontDownloadQueue"]
old-location: directwrite\idwritefontdownloadqueue.htm
tech.root: DirectWrite
ms.assetid: d1b1dfab-a22a-40bb-ffc4-eb094ac14217
ms.date: 09/10/2025
ms.keywords: IDWriteFontDownloadQueue, IDWriteFontDownloadQueue interface [Direct Write], IDWriteFontDownloadQueue interface [Direct Write],described, directwrite.idwritefontdownloadqueue, dwrite_3/IDWriteFontDownloadQueue
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
 - IDWriteFontDownloadQueue
 - dwrite_3/IDWriteFontDownloadQueue
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
 - IDWriteFontDownloadQueue
---

# IDWriteFontDownloadQueue interface


## -description

Interface that enqueues download requests for remote fonts, characters, glyphs, and font fragments.
        Provides methods to asynchronously execute a download, cancel pending downloads, and be notified of
        download completion. Callbacks to listeners will occur on the downloading thread, and objects must
        be must be able to handle calls on their methods from other threads at any time.

## -inheritance

The <b>IDWriteFontDownloadQueue</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontDownloadQueue</b> also has these types of members:

