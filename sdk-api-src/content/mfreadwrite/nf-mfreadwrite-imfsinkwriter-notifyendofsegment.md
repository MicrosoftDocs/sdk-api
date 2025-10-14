---
UID: NF:mfreadwrite.IMFSinkWriter.NotifyEndOfSegment
title: IMFSinkWriter::NotifyEndOfSegment (mfreadwrite.h)
description: Notifies the media sink that a stream has reached the end of a segment.
helpviewer_keywords: ["IMFSinkWriter interface [Media Foundation]","NotifyEndOfSegment method","IMFSinkWriter.NotifyEndOfSegment","IMFSinkWriter::NotifyEndOfSegment","NotifyEndOfSegment","NotifyEndOfSegment method [Media Foundation]","NotifyEndOfSegment method [Media Foundation]","IMFSinkWriter interface","mf.imfsinkwriter_notifyendofsegment","mfreadwrite/IMFSinkWriter::NotifyEndOfSegment"]
old-location: mf\imfsinkwriter_notifyendofsegment.htm
tech.root: mf
ms.assetid: cb5b76b4-ff08-4cac-bd30-d4f3b57acb78
ms.date: 12/05/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],NotifyEndOfSegment method, IMFSinkWriter.NotifyEndOfSegment, IMFSinkWriter::NotifyEndOfSegment, NotifyEndOfSegment, NotifyEndOfSegment method [Media Foundation], NotifyEndOfSegment method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_notifyendofsegment, mfreadwrite/IMFSinkWriter::NotifyEndOfSegment
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
 - IMFSinkWriter::NotifyEndOfSegment
 - mfreadwrite/IMFSinkWriter::NotifyEndOfSegment
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
 - IMFSinkWriter.NotifyEndOfSegment
---

# IMFSinkWriter::NotifyEndOfSegment


## -description

Notifies the media sink that a stream has reached the end of a segment.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of a stream, or <b>MF_SINK_WRITER_ALL_STREAMS</b> to signal that all streams have reached the end of a segment.

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

This method sends an <b>MFSTREAMSINK_MARKER_ENDOFSEGMENT</b> marker to the media sink for the specified streams. For more information, see <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker">IMFStreamSink::PlaceMarker</a>.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>