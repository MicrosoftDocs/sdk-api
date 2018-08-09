---
UID: NF:mfreadwrite.IMFSinkWriter.GetStatistics
title: IMFSinkWriter::GetStatistics
author: windows-sdk-content
description: Gets statistics about the performance of the sink writer.
old-location: mf\imfsinkwriter_getstatistics.htm
old-project: medfound
ms.assetid: 84028b1d-3843-4289-a04c-3039311d095b
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetStatistics, GetStatistics method [Media Foundation], GetStatistics method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],GetStatistics method, IMFSinkWriter.GetStatistics, IMFSinkWriter::GetStatistics, mf.imfsinkwriter_getstatistics, mfreadwrite/IMFSinkWriter::GetStatistics
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFSinkWriter.GetStatistics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSinkWriter::GetStatistics


## -description


Gets statistics about the performance of the sink writer.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of a stream to query, or <b>MF_SINK_WRITER_ALL_STREAMS </b> to query the media sink itself.


### -param pStats [out]

A pointer to an <a href="https://msdn.microsoft.com/ff083ae1-9a53-4215-9738-d1776f8d7f9b">MF_SINK_WRITER_STATISTICS</a> structure. Before calling the method, set the <b>cb</b> member to the size of the structure in bytes. The method fills the structure with statistics from the sink writer.


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




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

