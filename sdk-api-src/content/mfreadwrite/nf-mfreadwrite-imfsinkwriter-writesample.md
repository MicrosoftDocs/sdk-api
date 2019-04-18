---
UID: NF:mfreadwrite.IMFSinkWriter.WriteSample
title: IMFSinkWriter::WriteSample (mfreadwrite.h)
author: windows-sdk-content
description: Delivers a sample to the sink writer.
old-location: mf\imfsinkwriter_writesample.htm
tech.root: medfound
ms.assetid: 1c65a5d0-cc1b-456e-9d88-a24da57ee30a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],WriteSample method, IMFSinkWriter.WriteSample, IMFSinkWriter::WriteSample, WriteSample, WriteSample method [Media Foundation], WriteSample method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_writesample, mfreadwrite/IMFSinkWriter::WriteSample
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
 - IMFSinkWriter.WriteSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSinkWriter::WriteSample


## -description


Delivers a sample to the sink writer.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream for this sample.


### -param pSample [in]

A pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of the sample.


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

By default, the sink writer limits the rate of incoming data by blocking the calling thread inside the <b>WriteSample</b> method. This prevents the application from delivering samples too quickly. To disable this behavior, set the <a href="https://msdn.microsoft.com/eb79bda7-ece0-4977-a0f9-d40bd5d220ab">MF_SINK_WRITER_DISABLE_THROTTLING</a> attribute when you create the sink writer.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

