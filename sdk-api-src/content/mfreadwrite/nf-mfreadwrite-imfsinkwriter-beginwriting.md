---
UID: NF:mfreadwrite.IMFSinkWriter.BeginWriting
title: IMFSinkWriter::BeginWriting (mfreadwrite.h)
description: Initializes the sink writer for writing.
helpviewer_keywords: ["BeginWriting","BeginWriting method [Media Foundation]","BeginWriting method [Media Foundation]","IMFSinkWriter interface","IMFSinkWriter interface [Media Foundation]","BeginWriting method","IMFSinkWriter.BeginWriting","IMFSinkWriter::BeginWriting","mf.imfsinkwriter_beginwriting","mfreadwrite/IMFSinkWriter::BeginWriting"]
old-location: mf\imfsinkwriter_beginwriting.htm
tech.root: mf
ms.assetid: 32252658-662e-4d2f-a5fe-34f24ce60094
ms.date: 12/05/2018
ms.keywords: BeginWriting, BeginWriting method [Media Foundation], BeginWriting method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],BeginWriting method, IMFSinkWriter.BeginWriting, IMFSinkWriter::BeginWriting, mf.imfsinkwriter_beginwriting, mfreadwrite/IMFSinkWriter::BeginWriting
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
 - IMFSinkWriter::BeginWriting
 - mfreadwrite/IMFSinkWriter::BeginWriting
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
 - IMFSinkWriter.BeginWriting
---

# IMFSinkWriter::BeginWriting


## -description

Initializes the sink writer for writing.



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

Call this method after you configure the input streams and before you send any data to the sink writer. 

You must call <b>BeginWriting</b> before calling any of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize">IMFSinkWriter::Finalize</a>
</li>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-flush">IMFSinkWriter::Flush</a>
</li>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-notifyendofsegment">IMFSinkWriter::NotifyEndOfSegment</a>
</li>
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
The underlying media sink must have at least one input stream. Otherwise, <b>BeginWriting</b> returns <b>MF_E_INVALIDREQUEST</b>. To add input streams, call the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream">IMFSinkWriter::AddStream</a> method.

If <b>BeginWriting</b> succeeds, any further calls to <b>BeginWriting</b> return <b>MF_E_INVALIDREQUEST</b>.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>
