---
UID: NF:mfreadwrite.IMFSinkWriter.WriteSample
title: IMFSinkWriter::WriteSample (mfreadwrite.h)
description: Delivers a sample to the sink writer.
helpviewer_keywords: ["IMFSinkWriter interface [Media Foundation]","WriteSample method","IMFSinkWriter.WriteSample","IMFSinkWriter::WriteSample","WriteSample","WriteSample method [Media Foundation]","WriteSample method [Media Foundation]","IMFSinkWriter interface","mf.imfsinkwriter_writesample","mfreadwrite/IMFSinkWriter::WriteSample"]
old-location: mf\imfsinkwriter_writesample.htm
tech.root: mf
ms.assetid: 1c65a5d0-cc1b-456e-9d88-a24da57ee30a
ms.date: 12/05/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],WriteSample method, IMFSinkWriter.WriteSample, IMFSinkWriter::WriteSample, WriteSample, WriteSample method [Media Foundation], WriteSample method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_writesample, mfreadwrite/IMFSinkWriter::WriteSample
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
 - IMFSinkWriter::WriteSample
 - mfreadwrite/IMFSinkWriter::WriteSample
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
 - IMFSinkWriter.WriteSample
---

# IMFSinkWriter::WriteSample


## -description

Delivers a sample to the sink writer.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream for this sample.

### -param pSample [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of the sample.

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

By default, the sink writer limits the rate of incoming data by blocking the calling thread inside the <b>WriteSample</b> method. This prevents the application from delivering samples too quickly. To disable this behavior, set the <a href="/windows/desktop/medfound/mf-sink-writer-disable-throttling">MF_SINK_WRITER_DISABLE_THROTTLING</a> attribute when you create the sink writer.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>