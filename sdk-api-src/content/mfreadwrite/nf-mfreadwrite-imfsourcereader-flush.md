---
UID: NF:mfreadwrite.IMFSourceReader.Flush
title: IMFSourceReader::Flush
author: windows-sdk-content
description: Flushes one or more streams.
old-location: mf\imfsourcereader_flush.htm
tech.root: medfound
ms.assetid: 34992c64-9956-4b23-a979-df7f678405b5
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: Flush, Flush method [Media Foundation], Flush method [Media Foundation],IMFSourceReader interface, IMFSourceReader interface [Media Foundation],Flush method, IMFSourceReader.Flush, IMFSourceReader::Flush, MF_SOURCE_READER_ALL_STREAMS, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, mf.imfsourcereader_flush, mfreadwrite/IMFSourceReader::Flush
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
 - IMFSourceReader.Flush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceReader::Flush


## -description


Flushes one or more streams.


## -parameters




### -param dwStreamIndex [in]

The stream to flush. The value can be any of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0–0xFFFFFFFB</dt>
</dl>
</td>
<td width="60%">
The zero-based index of a stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_FIRST_VIDEO_STREAM"></a><a id="mf_source_reader_first_video_stream"></a><dl>
<dt><b><b>MF_SOURCE_READER_FIRST_VIDEO_STREAM</b></b></dt>
<dt>0xFFFFFFFC</dt>
</dl>
</td>
<td width="60%">
The first video stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_FIRST_AUDIO_STREAM"></a><a id="mf_source_reader_first_audio_stream"></a><dl>
<dt><b><b>MF_SOURCE_READER_FIRST_AUDIO_STREAM</b></b></dt>
<dt>0xFFFFFFFD</dt>
</dl>
</td>
<td width="60%">
The first audio stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_ALL_STREAMS"></a><a id="mf_source_reader_all_streams"></a><dl>
<dt><b><b>MF_SOURCE_READER_ALL_STREAMS</b></b></dt>
<dt>0xFFFFFFFE</dt>
</dl>
</td>
<td width="60%">
All streams.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>Flush</b> method discards all queued samples and cancels all pending sample requests.

This method can complete either synchronously or asynchronously.

If you provide a callback pointer when you create the source reader, the method is asynchronous. Otherwise, the method is synchronous. For more information about the setting the callback pointer, see <a href="https://msdn.microsoft.com/de226a5a-03c0-4bfe-bb20-8969ce43cf53">MF_SOURCE_READER_ASYNC_CALLBACK</a>.

In synchronous mode, the method blocks until the operation is complete.

In asynchronous mode, the application's <a href="https://msdn.microsoft.com/a8273b0a-a75a-453f-bb42-38d554e44262">IMFSourceReaderCallback::OnFlush</a> method is called when the flush operation completes. While a flush operation is pending, the <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a> method returns <b>MF_E_NOTACCEPTING</b>.

<div class="alert"><b>Note</b>  In Windows 7, there was a bug in the implementation of this method, which causes <a href="https://msdn.microsoft.com/a8273b0a-a75a-453f-bb42-38d554e44262">OnFlush</a> to be called before the flush operation completes. A hotfix is available that fixes this bug. For more information, see <a href="http://support.microsoft.com/kb/979567">http://support.microsoft.com/kb/979567</a>.</div>
<div> </div>
This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

