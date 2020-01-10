---
UID: NN:mfreadwrite.IMFSinkWriter
title: IMFSinkWriter (mfreadwrite.h)
description: Implemented by the Microsoft Media Foundation sink writer object.
old-location: mf\imfsinkwriter.htm
tech.root: medfound
ms.assetid: 76fb915e-1586-429a-88a5-bd1290799352
ms.date: 12/05/2018
ms.keywords: IMFSinkWriter, IMFSinkWriter interface [Media Foundation], IMFSinkWriter interface [Media Foundation],described, mf.imfsinkwriter, mfreadwrite/IMFSinkWriter
f1_keywords:
- mfreadwrite/IMFSinkWriter
dev_langs:
- c++
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
- IMFSinkWriter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSinkWriter interface


## -description


Implemented by the Microsoft Media Foundation sink writer object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSinkWriter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSinkWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSinkWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the sink writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting">BeginWriting</a>
</td>
<td align="left" width="63%">
Initializes the sink writer for writing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize">Finalize</a>
</td>
<td align="left" width="63%">
Completes all writing operations on the sink writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-flush">Flush</a>
</td>
<td align="left" width="63%">
Flushes one or more streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-getserviceforstream">GetServiceForStream</a>
</td>
<td align="left" width="63%">
Queries the underlying media sink or encoder for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-getstatistics">GetStatistics</a>
</td>
<td align="left" width="63%">
Gets statistics about the performance of the sink writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-notifyendofsegment">NotifyEndOfSegment</a>
</td>
<td align="left" width="63%">
 Notifies the media sink that a stream has reached the end of a segment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-placemarker">PlaceMarker</a>
</td>
<td align="left" width="63%">
Places a marker in the specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-sendstreamtick">SendStreamTick</a>
</td>
<td align="left" width="63%">
Indicates a gap in an input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype">SetInputMediaType</a>
</td>
<td align="left" width="63%">
Sets the input format for a stream on the sink writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample">WriteSample</a>
</td>
<td align="left" width="63%">
Delivers a sample to the sink writer.

</td>
</tr>
</table> 


## -remarks



To create the sink writer, call one of the following functions:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink">MFCreateSinkWriterFromMediaSink</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl">MFCreateSinkWriterFromURL</a>
</li>
</ul>
Alternatively, use the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory">IMFReadWriteClassFactory</a> interface.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

In Windows 8, this interface is extended with <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex">IMFSinkWriterEx</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/sink-writer">Sink Writer</a>
 

 

