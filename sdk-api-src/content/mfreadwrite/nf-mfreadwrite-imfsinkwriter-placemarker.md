---
UID: NF:mfreadwrite.IMFSinkWriter.PlaceMarker
title: IMFSinkWriter::PlaceMarker
author: windows-sdk-content
description: Places a marker in the specified stream.
old-location: mf\imfsinkwriter_placemarker.htm
tech.root: medfound
ms.assetid: 93140993-a926-437e-bc40-9b011c4c6832
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],PlaceMarker method, IMFSinkWriter.PlaceMarker, IMFSinkWriter::PlaceMarker, PlaceMarker, PlaceMarker method [Media Foundation], PlaceMarker method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_placemarker, mfreadwrite/IMFSinkWriter::PlaceMarker
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSinkWriter.PlaceMarker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriter::PlaceMarker


## -description


Places a marker in the specified stream.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream.


### -param pvContext [in]

Pointer to an application-defined value. The value of this parameter is returned to the caller in the <i>pvContext</i>  parameter of the caller's <a href="https://msdn.microsoft.com/5b1ca6a7-c2bc-4b30-aa86-05bd4ccc052c">IMFSinkWriterCallback::OnMarker</a> callback method. The application is responsible for any memory allocation associated with this data. This parameter can be <b>NULL</b>. 


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDREQUEST</b></b></dt>
</dl>
</td>
<td width="60%">
The request is invalid.

</td>
</tr>
</table>
 




## -remarks



To use this method, you must provide an asynchronous callback when you create the sink writer. Otherwise, the method returns <b>MF_E_INVALIDREQUEST</b>. For more information, see <a href="https://msdn.microsoft.com/22df1fa0-469d-4501-aaf0-a0379b7ed096">MF_SINK_WRITER_ASYNC_CALLBACK</a>.

Markers provide a way to be notified when the media sink consumes all of the samples in a stream up to a certain point. The media sink does not process the marker until it has processed all of the samples that came before the marker. When the media sink processes the marker, the sink writer calls the application's <a href="https://msdn.microsoft.com/5b1ca6a7-c2bc-4b30-aa86-05bd4ccc052c">OnMarker</a> method. When the callback is invoked, you know that the sink has consumed all of the previous samples for that stream.

For example, to change the format midstream, call <b>PlaceMarker</b> at the point where the format changes. When <a href="https://msdn.microsoft.com/5b1ca6a7-c2bc-4b30-aa86-05bd4ccc052c">OnMarker</a> is called, it is safe to call <a href="https://msdn.microsoft.com/02a73f73-3b25-4578-9a7e-c9f8a4c8cd99">IMFSinkWriter::SetInputMediaType</a> to change the input type (assuming that the media sink supports dynamic format changes).

Internally, this method calls <a href="https://msdn.microsoft.com/bfa4fb12-59b2-4599-b8ff-dc38750a5a79">IMFStreamSink::PlaceMarker</a> on the media sink.


<div class="alert"><b>Note</b>  The <i>pvContext</i> parameter of the <b>IMFSinkWriter::PlaceMarker</b> method is not passed to the <i>pvarContextValue</i> parameter of the <a href="https://msdn.microsoft.com/bfa4fb12-59b2-4599-b8ff-dc38750a5a79">IMFStreamSink::PlaceMarker</a> method. These two parameters are not directly related.</div>
<div> </div>


This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

