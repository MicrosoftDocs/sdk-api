---
UID: NN:mfreadwrite.IMFSourceReaderCallback
title: IMFSourceReaderCallback (mfreadwrite.h)
description: Callback interface for the Microsoft Media Foundation source reader.
helpviewer_keywords: ["IMFSourceReaderCallback","IMFSourceReaderCallback interface [Media Foundation]","IMFSourceReaderCallback interface [Media Foundation]","described","mf.imfsourcereadercallback","mfreadwrite/IMFSourceReaderCallback"]
old-location: mf\imfsourcereadercallback.htm
tech.root: mf
ms.assetid: fff8b6e6-5d56-4301-b3ce-f3ff49398593
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderCallback, IMFSourceReaderCallback interface [Media Foundation], IMFSourceReaderCallback interface [Media Foundation],described, mf.imfsourcereadercallback, mfreadwrite/IMFSourceReaderCallback
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceReaderCallback
 - mfreadwrite/IMFSourceReaderCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSourceReaderCallback
---

# IMFSourceReaderCallback interface


## -description

Callback interface for the Microsoft Media Foundation source reader.

## -inheritance

The <b>IMFSourceReaderCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceReaderCallback</b> also has these types of members:

## -remarks

Use the <a href="/windows/desktop/medfound/mf-source-reader-async-callback">MF_SOURCE_READER_ASYNC_CALLBACK</a> attribute to set the callback pointer when you first create the source reader object.

The callback methods can be called from any thread, so an object that implements this interface must be thread-safe.

If you do not specify a callback pointer, the source reader operates synchronously.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>



<a href="/windows/desktop/medfound/using-the-source-reader-in-asynchronous-mode">Using the Source Reader in Asynchronous Mode</a>
