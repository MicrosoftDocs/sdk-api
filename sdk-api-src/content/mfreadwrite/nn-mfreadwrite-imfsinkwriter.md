---
UID: NN:mfreadwrite.IMFSinkWriter
title: IMFSinkWriter
author: windows-sdk-content
description: Implemented by the Microsoft Media Foundation sink writer object.
old-location: mf\imfsinkwriter.htm
tech.root: medfound
ms.assetid: 76fb915e-1586-429a-88a5-bd1290799352
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFSinkWriter, IMFSinkWriter interface [Media Foundation], IMFSinkWriter interface [Media Foundation],described, mf.imfsinkwriter, mfreadwrite/IMFSinkWriter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriter interface


## -description


Implemented by the Microsoft Media Foundation sink writer object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSinkWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSinkWriter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9f9b1216-e915-4188-bcfd-6c41e1821ec4">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the sink writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32252658-662e-4d2f-a5fe-34f24ce60094">BeginWriting</a>
</td>
<td align="left" width="63%">
Initializes the sink writer for writing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/352e6679-0710-429a-a659-47044ab60773">Finalize</a>
</td>
<td align="left" width="63%">
Completes all writing operations on the sink writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/997235cb-6ca5-434c-81a6-7a294e0cccca">Flush</a>
</td>
<td align="left" width="63%">
Flushes one or more streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/166f8f71-e52d-43b1-9137-e4bf79bf5421">GetServiceForStream</a>
</td>
<td align="left" width="63%">
Queries the underlying media sink or encoder for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84028b1d-3843-4289-a04c-3039311d095b">GetStatistics</a>
</td>
<td align="left" width="63%">
Gets statistics about the performance of the sink writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb5b76b4-ff08-4cac-bd30-d4f3b57acb78">NotifyEndOfSegment</a>
</td>
<td align="left" width="63%">
 Notifies the media sink that a stream has reached the end of a segment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93140993-a926-437e-bc40-9b011c4c6832">PlaceMarker</a>
</td>
<td align="left" width="63%">
Places a marker in the specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b4b76b7-1a39-4323-94e7-0b2d159a8038">SendStreamTick</a>
</td>
<td align="left" width="63%">
Indicates a gap in an input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02a73f73-3b25-4578-9a7e-c9f8a4c8cd99">SetInputMediaType</a>
</td>
<td align="left" width="63%">
Sets the input format for a stream on the sink writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c65a5d0-cc1b-456e-9d88-a24da57ee30a">WriteSample</a>
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
<a href="https://msdn.microsoft.com/77bd81fe-bcbd-4bcd-9d3a-dd9fe6154337">MFCreateSinkWriterFromMediaSink</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ac6a30c7-5e44-453a-8114-8d7d65332024">MFCreateSinkWriterFromURL</a>
</li>
</ul>
Alternatively, use the <a href="https://msdn.microsoft.com/83ef0f0a-ae60-474d-a9e7-7c83a73f6255">IMFReadWriteClassFactory</a> interface.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

In Windows 8, this interface is extended with <a href="https://msdn.microsoft.com/77E6CB22-E3B5-4D5E-8876-48582F75AA5C">IMFSinkWriterEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

