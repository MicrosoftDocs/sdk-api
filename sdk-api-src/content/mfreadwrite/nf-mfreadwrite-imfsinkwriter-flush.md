---
UID: NF:mfreadwrite.IMFSinkWriter.Flush
title: IMFSinkWriter::Flush (mfreadwrite.h)
description: Flushes one or more streams. (IMFSinkWriter.Flush)
helpviewer_keywords: ["Flush","Flush method [Media Foundation]","Flush method [Media Foundation]","IMFSinkWriter interface","IMFSinkWriter interface [Media Foundation]","Flush method","IMFSinkWriter.Flush","IMFSinkWriter::Flush","mf.imfsinkwriter_flush","mfreadwrite/IMFSinkWriter::Flush"]
old-location: mf\imfsinkwriter_flush.htm
tech.root: mf
ms.assetid: 997235cb-6ca5-434c-81a6-7a294e0cccca
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [Media Foundation], Flush method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],Flush method, IMFSinkWriter.Flush, IMFSinkWriter::Flush, mf.imfsinkwriter_flush, mfreadwrite/IMFSinkWriter::Flush
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
 - IMFSinkWriter::Flush
 - mfreadwrite/IMFSinkWriter::Flush
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
 - IMFSinkWriter.Flush
---

# IMFSinkWriter::Flush


## -description

Flushes one or more streams.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream to flush, or <b>MF_SINK_WRITER_ALL_STREAMS</b> to flush all of the streams.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The request is invalid.

</td>
</tr>
</table>

## -remarks

You must call <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting">IMFSinkWriter::BeginWriting</a> before calling this method. Otherwise, the method returns <b>MF_E_INVALIDREQUEST</b>.

For each stream that is flushed, the sink writer drops all pending samples, flushes the encoder, and sends an <b>MFSTREAMSINK_MARKER_ENDOFSEGMENT</b> marker to the media sink.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>
