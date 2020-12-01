---
UID: NF:mfreadwrite.IMFSourceReaderCallback.OnFlush
title: IMFSourceReaderCallback::OnFlush (mfreadwrite.h)
description: Called when the IMFSourceReader::Flush method completes.
helpviewer_keywords: ["IMFSourceReaderCallback interface [Media Foundation]","OnFlush method","IMFSourceReaderCallback.OnFlush","IMFSourceReaderCallback::OnFlush","OnFlush","OnFlush method [Media Foundation]","OnFlush method [Media Foundation]","IMFSourceReaderCallback interface","mf.imfsourcereadercallback_onflush","mfreadwrite/IMFSourceReaderCallback::OnFlush"]
old-location: mf\imfsourcereadercallback_onflush.htm
tech.root: mf
ms.assetid: a8273b0a-a75a-453f-bb42-38d554e44262
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderCallback interface [Media Foundation],OnFlush method, IMFSourceReaderCallback.OnFlush, IMFSourceReaderCallback::OnFlush, OnFlush, OnFlush method [Media Foundation], OnFlush method [Media Foundation],IMFSourceReaderCallback interface, mf.imfsourcereadercallback_onflush, mfreadwrite/IMFSourceReaderCallback::OnFlush
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
 - IMFSourceReaderCallback::OnFlush
 - mfreadwrite/IMFSourceReaderCallback::OnFlush
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
 - IMFSourceReaderCallback.OnFlush
---

# IMFSourceReaderCallback::OnFlush


## -description

Called when the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush">IMFSourceReader::Flush</a> method completes.

## -parameters

### -param dwStreamIndex

The index of the stream that was flushed, or <b>MF_SOURCE_READER_ALL_STREAMS</b> if all streams were flushed.

## -returns

Returns an <b>HRESULT</b> value. Currently, the source reader ignores the return value.

## -remarks

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback">IMFSourceReaderCallback</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>