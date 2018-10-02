---
UID: NF:mfreadwrite.IMFSinkWriter.NotifyEndOfSegment
title: IMFSinkWriter::NotifyEndOfSegment
author: windows-sdk-content
description: Notifies the media sink that a stream has reached the end of a segment.
old-location: mf\imfsinkwriter_notifyendofsegment.htm
tech.root: MedFound
ms.assetid: cb5b76b4-ff08-4cac-bd30-d4f3b57acb78
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],NotifyEndOfSegment method, IMFSinkWriter.NotifyEndOfSegment, IMFSinkWriter::NotifyEndOfSegment, NotifyEndOfSegment, NotifyEndOfSegment method [Media Foundation], NotifyEndOfSegment method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_notifyendofsegment, mfreadwrite/IMFSinkWriter::NotifyEndOfSegment
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
 - IMFSinkWriter.NotifyEndOfSegment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



You must call <a href="https://msdn.microsoft.com/32252658-662e-4d2f-a5fe-34f24ce60094">IMFSinkWriter::BeginWriting</a> before calling this method. Otherwise, the method returns <b>MF_E_INVALIDREQUEST</b>.

This method sends an <b>MFSTREAMSINK_MARKER_ENDOFSEGMENT</b> marker to the media sink for the specified streams. For more information, see <a href="https://msdn.microsoft.com/bfa4fb12-59b2-4599-b8ff-dc38750a5a79">IMFStreamSink::PlaceMarker</a>.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

