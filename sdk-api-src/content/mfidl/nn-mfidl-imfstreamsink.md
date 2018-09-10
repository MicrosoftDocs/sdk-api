---
UID: NN:mfidl.IMFStreamSink
title: IMFStreamSink
author: windows-sdk-content
description: Represents a stream on a media sink object.
old-location: mf\imfstreamsink.htm
tech.root: medfound
ms.assetid: fe403cab-b901-4c8e-a23c-788ee65c4689
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFStreamSink, IMFStreamSink interface [Media Foundation], IMFStreamSink interface [Media Foundation],described, fe403cab-b901-4c8e-a23c-788ee65c4689, mf.imfstreamsink, mfidl/IMFStreamSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFStreamSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFStreamSink interface


## -description


Represents a stream on a media sink object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFStreamSink</b> interface inherits from <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>. <b>IMFStreamSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFStreamSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/514d29bd-571d-46b1-9948-5d623c6703aa">Flush</a>
</td>
<td align="left" width="63%">
Causes the stream sink to drop any samples that it has received and has not rendered yet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af4855f6-36fa-4949-8b93-9e630a12e71b">GetIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the stream identifier for this stream sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/799fb0ce-6a43-49c2-97cf-49c51d8f69cd">GetMediaSink</a>
</td>
<td align="left" width="63%">
Retrieves the media sink that owns this stream sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/819d06b1-6b52-4496-bed8-a08b8f0b6153">GetMediaTypeHandler</a>
</td>
<td align="left" width="63%">
Retrieves the media type handler for the stream sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfa4fb12-59b2-4599-b8ff-dc38750a5a79">PlaceMarker</a>
</td>
<td align="left" width="63%">
Places a marker in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30e2bdb5-a99d-4a2e-ab36-7b4e383c645f">ProcessSample</a>
</td>
<td align="left" width="63%">
Delivers a sample to the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

