---
UID: NF:mfreadwrite.IMFSinkWriter.SendStreamTick
title: IMFSinkWriter::SendStreamTick (mfreadwrite.h)
description: Indicates a gap in an input stream.
helpviewer_keywords: ["IMFSinkWriter interface [Media Foundation]","SendStreamTick method","IMFSinkWriter.SendStreamTick","IMFSinkWriter::SendStreamTick","SendStreamTick","SendStreamTick method [Media Foundation]","SendStreamTick method [Media Foundation]","IMFSinkWriter interface","mf.imfsinkwriter_sendstreamtick","mfreadwrite/IMFSinkWriter::SendStreamTick"]
old-location: mf\imfsinkwriter_sendstreamtick.htm
tech.root: mf
ms.assetid: 3b4b76b7-1a39-4323-94e7-0b2d159a8038
ms.date: 12/05/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],SendStreamTick method, IMFSinkWriter.SendStreamTick, IMFSinkWriter::SendStreamTick, SendStreamTick, SendStreamTick method [Media Foundation], SendStreamTick method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_sendstreamtick, mfreadwrite/IMFSinkWriter::SendStreamTick
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
 - IMFSinkWriter::SendStreamTick
 - mfreadwrite/IMFSinkWriter::SendStreamTick
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
 - IMFSinkWriter.SendStreamTick
---

# IMFSinkWriter::SendStreamTick


## -description

Indicates a gap in an input stream.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream.

### -param llTimestamp [in]

The position in the stream where the gap in the data occurs. The value is given in 100-nanosecond units, relative to the start of the stream.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For video, call this method once for each missing frame. For audio, call this method at least once per second during a gap in the audio. Set the <a href="/windows/desktop/medfound/mfsampleextension-discontinuity-attribute">MFSampleExtension_Discontinuity</a> attribute on the first media sample after the gap.

Internally, this method calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker">IMFStreamSink::PlaceMarker</a> on the media sink.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>