---
UID: NF:mfreadwrite.IMFSinkWriter.Flush
title: IMFSinkWriter::Flush
author: windows-driver-content
description: Flushes one or more streams.
old-location: mf\imfsinkwriter_flush.htm
old-project: medfound
ms.assetid: 997235cb-6ca5-434c-81a6-7a294e0cccca
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: Flush, Flush method [Media Foundation], Flush method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],Flush method, IMFSinkWriter.Flush, IMFSinkWriter::Flush, mf.imfsinkwriter_flush, mfreadwrite/IMFSinkWriter::Flush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFSinkWriter.Flush
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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

For each stream that is flushed, the sink writer drops all pending samples, flushes the encoder, and sends an <b>MFSTREAMSINK_MARKER_ENDOFSEGMENT</b> marker to the media sink.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

