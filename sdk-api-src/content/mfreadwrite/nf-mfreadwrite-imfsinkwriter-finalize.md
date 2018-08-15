---
UID: NF:mfreadwrite.IMFSinkWriter.Finalize
title: IMFSinkWriter::Finalize
author: windows-sdk-content
description: Completes all writing operations on the sink writer.
old-location: mf\imfsinkwriter_finalize.htm
old-project: medfound
ms.assetid: 352e6679-0710-429a-a659-47044ab60773
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: Finalize, Finalize method [Media Foundation], Finalize method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],Finalize method, IMFSinkWriter.Finalize, IMFSinkWriter::Finalize, mf.imfsinkwriter_finalize, mfreadwrite/IMFSinkWriter::Finalize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSinkWriter.Finalize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSinkWriter::Finalize


## -description


Completes all writing operations on the sink writer.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method after you send all of the input samples to the sink writer. The method performs any operations needed to create the final output from the media sink.

If you provide a callback interface when you create the sink writer, this method completes asynchronously. When the operation completes, the <a href="https://msdn.microsoft.com/9da7bb55-bf9f-4579-ae8e-b33ce5461950">IMFSinkWriterCallback::OnFinalize</a> method of your callback is called. For more information, see <a href="https://msdn.microsoft.com/22df1fa0-469d-4501-aaf0-a0379b7ed096">MF_SINK_WRITER_ASYNC_CALLBACK</a>.  Otherwise, if you do not provide a callback, the <b>Finalize</b> method blocks until the operation completes.

Internally, this method calls <a href="https://msdn.microsoft.com/bfa4fb12-59b2-4599-b8ff-dc38750a5a79">IMFStreamSink::PlaceMarker</a> to place end-of-segment markers for each stream on the media sink. It also calls <a href="https://msdn.microsoft.com/fbcb7722-ba64-40a6-9c43-26a6b8dce7f6">IMFFinalizableMediaSink::BeginFinalize</a> and <a href="https://msdn.microsoft.com/1b2a9b24-69da-41c7-8379-3f3d066d2582">EndFinalize</a> if the media sink supports the <a href="https://msdn.microsoft.com/e60c2773-f2fc-469e-a698-036390cbed16">IMFFinalizableMediaSink</a> interface.

After this method is called, the following methods will fail:

<ul>
<li>
<a href="https://msdn.microsoft.com/93140993-a926-437e-bc40-9b011c4c6832">IMFSinkWriter::PlaceMarker</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3b4b76b7-1a39-4323-94e7-0b2d159a8038">IMFSinkWriter::SendStreamTick</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1c65a5d0-cc1b-456e-9d88-a24da57ee30a">IMFSinkWriter::WriteSample</a>
</li>
</ul>
If you do not call <b>Finalize</b>, the output from the media sink might be incomplete or invalid. For example, required file headers might be missing from the output file.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

