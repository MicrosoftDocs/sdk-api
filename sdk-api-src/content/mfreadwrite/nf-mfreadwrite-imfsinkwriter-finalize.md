---
UID: NF:mfreadwrite.IMFSinkWriter.Finalize
title: IMFSinkWriter::Finalize (mfreadwrite.h)
description: Completes all writing operations on the sink writer.
helpviewer_keywords: ["Finalize","Finalize method [Media Foundation]","Finalize method [Media Foundation]","IMFSinkWriter interface","IMFSinkWriter interface [Media Foundation]","Finalize method","IMFSinkWriter.Finalize","IMFSinkWriter::Finalize","mf.imfsinkwriter_finalize","mfreadwrite/IMFSinkWriter::Finalize"]
old-location: mf\imfsinkwriter_finalize.htm
tech.root: mf
ms.assetid: 352e6679-0710-429a-a659-47044ab60773
ms.date: 12/05/2018
ms.keywords: Finalize, Finalize method [Media Foundation], Finalize method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],Finalize method, IMFSinkWriter.Finalize, IMFSinkWriter::Finalize, mf.imfsinkwriter_finalize, mfreadwrite/IMFSinkWriter::Finalize
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
 - IMFSinkWriter::Finalize
 - mfreadwrite/IMFSinkWriter::Finalize
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
 - IMFSinkWriter.Finalize
---

# IMFSinkWriter::Finalize


## -description

Completes all writing operations on the sink writer.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method after you send all of the input samples to the sink writer. The method performs any operations needed to create the final output from the media sink.

If you provide a callback interface when you create the sink writer, this method completes asynchronously. When the operation completes, the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwritercallback-onfinalize">IMFSinkWriterCallback::OnFinalize</a> method of your callback is called. For more information, see <a href="/windows/desktop/medfound/mf-sink-writer-async-callback">MF_SINK_WRITER_ASYNC_CALLBACK</a>.  Otherwise, if you do not provide a callback, the <b>Finalize</b> method blocks until the operation completes.

Internally, this method calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker">IMFStreamSink::PlaceMarker</a> to place end-of-segment markers for each stream on the media sink. It also calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize">IMFFinalizableMediaSink::BeginFinalize</a> and <a href="/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-endfinalize">EndFinalize</a> if the media sink supports the <a href="/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink">IMFFinalizableMediaSink</a> interface.

After this method is called, the following methods will fail:

<ul>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-placemarker">IMFSinkWriter::PlaceMarker</a>
</li>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-sendstreamtick">IMFSinkWriter::SendStreamTick</a>
</li>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample">IMFSinkWriter::WriteSample</a>
</li>
</ul>
If you do not call <b>Finalize</b>, the output from the media sink might be incomplete or invalid. For example, required file headers might be missing from the output file.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>
