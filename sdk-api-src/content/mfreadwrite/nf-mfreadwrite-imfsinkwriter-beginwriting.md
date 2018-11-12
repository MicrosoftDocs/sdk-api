---
UID: NF:mfreadwrite.IMFSinkWriter.BeginWriting
title: IMFSinkWriter::BeginWriting
author: windows-sdk-content
description: Initializes the sink writer for writing.
old-location: mf\imfsinkwriter_beginwriting.htm
tech.root: medfound
ms.assetid: 32252658-662e-4d2f-a5fe-34f24ce60094
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: BeginWriting, BeginWriting method [Media Foundation], BeginWriting method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],BeginWriting method, IMFSinkWriter.BeginWriting, IMFSinkWriter::BeginWriting, mf.imfsinkwriter_beginwriting, mfreadwrite/IMFSinkWriter::BeginWriting
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
 - IMFSinkWriter.BeginWriting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriter::BeginWriting


## -description


Initializes the sink writer for writing.


## -parameters






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



Call this method after you configure the input streams and before you send any data to the sink writer. 

You must call <b>BeginWriting</b> before calling any of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/352e6679-0710-429a-a659-47044ab60773">IMFSinkWriter::Finalize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/997235cb-6ca5-434c-81a6-7a294e0cccca">IMFSinkWriter::Flush</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cb5b76b4-ff08-4cac-bd30-d4f3b57acb78">IMFSinkWriter::NotifyEndOfSegment</a>
</li>
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
The underlying media sink must have at least one input stream. Otherwise, <b>BeginWriting</b> returns <b>MF_E_INVALIDREQUEST</b>. To add input streams, call the <a href="https://msdn.microsoft.com/9f9b1216-e915-4188-bcfd-6c41e1821ec4">IMFSinkWriter::AddStream</a> method.

If <b>BeginWriting</b> succeeds, any further calls to <b>BeginWriting</b> return <b>MF_E_INVALIDREQUEST</b>.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

