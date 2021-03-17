---
UID: NF:mfreadwrite.IMFSinkWriter.GetStatistics
title: IMFSinkWriter::GetStatistics (mfreadwrite.h)
description: Gets statistics about the performance of the sink writer.
helpviewer_keywords: ["GetStatistics","GetStatistics method [Media Foundation]","GetStatistics method [Media Foundation]","IMFSinkWriter interface","IMFSinkWriter interface [Media Foundation]","GetStatistics method","IMFSinkWriter.GetStatistics","IMFSinkWriter::GetStatistics","mf.imfsinkwriter_getstatistics","mfreadwrite/IMFSinkWriter::GetStatistics"]
old-location: mf\imfsinkwriter_getstatistics.htm
tech.root: mf
ms.assetid: 84028b1d-3843-4289-a04c-3039311d095b
ms.date: 12/05/2018
ms.keywords: GetStatistics, GetStatistics method [Media Foundation], GetStatistics method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],GetStatistics method, IMFSinkWriter.GetStatistics, IMFSinkWriter::GetStatistics, mf.imfsinkwriter_getstatistics, mfreadwrite/IMFSinkWriter::GetStatistics
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
 - IMFSinkWriter::GetStatistics
 - mfreadwrite/IMFSinkWriter::GetStatistics
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
 - IMFSinkWriter.GetStatistics
---

# IMFSinkWriter::GetStatistics


## -description

Gets statistics about the performance of the sink writer.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of a stream to query, or <b>MF_SINK_WRITER_ALL_STREAMS </b> to query the media sink itself.

### -param pStats [out]

A pointer to an <a href="/windows/desktop/api/mfreadwrite/ns-mfreadwrite-mf_sink_writer_statistics">MF_SINK_WRITER_STATISTICS</a> structure. Before calling the method, set the <b>cb</b> member to the size of the structure in bytes. The method fills the structure with statistics from the sink writer.

## -returns

This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number.

</td>
</tr>
</table>

## -remarks

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>