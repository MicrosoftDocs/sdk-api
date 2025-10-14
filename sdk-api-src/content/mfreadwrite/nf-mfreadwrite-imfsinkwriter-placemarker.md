---
UID: NF:mfreadwrite.IMFSinkWriter.PlaceMarker
title: IMFSinkWriter::PlaceMarker (mfreadwrite.h)
description: Places a marker in the specified stream.
helpviewer_keywords: ["IMFSinkWriter interface [Media Foundation]","PlaceMarker method","IMFSinkWriter.PlaceMarker","IMFSinkWriter::PlaceMarker","PlaceMarker","PlaceMarker method [Media Foundation]","PlaceMarker method [Media Foundation]","IMFSinkWriter interface","mf.imfsinkwriter_placemarker","mfreadwrite/IMFSinkWriter::PlaceMarker"]
old-location: mf\imfsinkwriter_placemarker.htm
tech.root: mf
ms.assetid: 93140993-a926-437e-bc40-9b011c4c6832
ms.date: 12/05/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],PlaceMarker method, IMFSinkWriter.PlaceMarker, IMFSinkWriter::PlaceMarker, PlaceMarker, PlaceMarker method [Media Foundation], PlaceMarker method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_placemarker, mfreadwrite/IMFSinkWriter::PlaceMarker
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
 - IMFSinkWriter::PlaceMarker
 - mfreadwrite/IMFSinkWriter::PlaceMarker
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
 - IMFSinkWriter.PlaceMarker
---

# IMFSinkWriter::PlaceMarker


## -description

Places a marker in the specified stream.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream.

### -param pvContext [in]

Pointer to an application-defined value. The value of this parameter is returned to the caller in the <i>pvContext</i>  parameter of the caller's <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwritercallback-onmarker">IMFSinkWriterCallback::OnMarker</a> callback method. The application is responsible for any memory allocation associated with this data. This parameter can be <b>NULL</b>.

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

To use this method, you must provide an asynchronous callback when you create the sink writer. Otherwise, the method returns <b>MF_E_INVALIDREQUEST</b>. For more information, see <a href="/windows/desktop/medfound/mf-sink-writer-async-callback">MF_SINK_WRITER_ASYNC_CALLBACK</a>.

Markers provide a way to be notified when the media sink consumes all of the samples in a stream up to a certain point. The media sink does not process the marker until it has processed all of the samples that came before the marker. When the media sink processes the marker, the sink writer calls the application's <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwritercallback-onmarker">OnMarker</a> method. When the callback is invoked, you know that the sink has consumed all of the previous samples for that stream.

For example, to change the format midstream, call <b>PlaceMarker</b> at the point where the format changes. When <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwritercallback-onmarker">OnMarker</a> is called, it is safe to call <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype">IMFSinkWriter::SetInputMediaType</a> to change the input type (assuming that the media sink supports dynamic format changes).

Internally, this method calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker">IMFStreamSink::PlaceMarker</a> on the media sink.


<div class="alert"><b>Note</b>  The <i>pvContext</i> parameter of the <b>IMFSinkWriter::PlaceMarker</b> method is not passed to the <i>pvarContextValue</i> parameter of the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker">IMFStreamSink::PlaceMarker</a> method. These two parameters are not directly related.</div>
<div> </div>


This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>