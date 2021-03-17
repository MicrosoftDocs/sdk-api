---
UID: NF:mfreadwrite.IMFSourceReaderCallback.OnReadSample
title: IMFSourceReaderCallback::OnReadSample (mfreadwrite.h)
description: Called when the IMFSourceReader::ReadSample method completes.
helpviewer_keywords: ["IMFSourceReaderCallback interface [Media Foundation]","OnReadSample method","IMFSourceReaderCallback.OnReadSample","IMFSourceReaderCallback::OnReadSample","OnReadSample","OnReadSample method [Media Foundation]","OnReadSample method [Media Foundation]","IMFSourceReaderCallback interface","mf.imfsourcereadercallback_onreadsample","mfreadwrite/IMFSourceReaderCallback::OnReadSample"]
old-location: mf\imfsourcereadercallback_onreadsample.htm
tech.root: mf
ms.assetid: 1f334b49-d297-478d-a037-2fc53a75ed52
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderCallback interface [Media Foundation],OnReadSample method, IMFSourceReaderCallback.OnReadSample, IMFSourceReaderCallback::OnReadSample, OnReadSample, OnReadSample method [Media Foundation], OnReadSample method [Media Foundation],IMFSourceReaderCallback interface, mf.imfsourcereadercallback_onreadsample, mfreadwrite/IMFSourceReaderCallback::OnReadSample
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
 - IMFSourceReaderCallback::OnReadSample
 - mfreadwrite/IMFSourceReaderCallback::OnReadSample
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
 - IMFSourceReaderCallback.OnReadSample
---

# IMFSourceReaderCallback::OnReadSample


## -description

Called when the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample">IMFSourceReader::ReadSample</a> method completes.

## -parameters

### -param hrStatus [in]

The status code. If an error occurred while processing the next sample, this parameter contains the error code.

### -param dwStreamIndex [in]

The zero-based index of the stream that delivered the sample.

### -param dwStreamFlags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag">MF_SOURCE_READER_FLAG</a> enumeration.

### -param llTimestamp [in]

The time stamp of the sample, or the time of the stream event indicated in <i>dwStreamFlags</i>. The time is given in 100-nanosecond units.

### -param pSample [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of a media sample. This parameter might be <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value. Currently, the source reader ignores the return value.

## -remarks

The <i>pSample</i> parameter might be <b>NULL</b>. For example, when the source reader reaches the end of a stream, <i>dwStreamFlags</i> contains the <b>MF_SOURCE_READERF_ENDOFSTREAM</b> flag, and <i>pSample</i> is <b>NULL</b>.



If there is a gap in the stream, <i>dwStreamFlags</i> contains the <b>MF_SOURCE_READERF_STREAMTICK</b> flag, <i>pSample</i> is <b>NULL</b>, and <i>llTimestamp</i> indicates the time when the gap occurred. 



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback">IMFSourceReaderCallback</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>