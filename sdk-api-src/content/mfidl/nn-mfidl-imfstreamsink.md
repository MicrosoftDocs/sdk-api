---
UID: NN:mfidl.IMFStreamSink
title: IMFStreamSink (mfidl.h)
author: windows-sdk-content
description: Represents a stream on a media sink object.
old-location: mf\imfstreamsink.htm
tech.root: medfound
ms.assetid: fe403cab-b901-4c8e-a23c-788ee65c4689
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFStreamSink, IMFStreamSink interface [Media Foundation], IMFStreamSink interface [Media Foundation],described, fe403cab-b901-4c8e-a23c-788ee65c4689, mf.imfstreamsink, mfidl/IMFStreamSink
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFStreamSink"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFStreamSink interface


## -description


Represents a stream on a media sink object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFStreamSink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>. <b>IMFStreamSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-flush">Flush</a>
</td>
<td align="left" width="63%">
Causes the stream sink to drop any samples that it has received and has not rendered yet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getidentifier">GetIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the stream identifier for this stream sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediasink">GetMediaSink</a>
</td>
<td align="left" width="63%">
Retrieves the media sink that owns this stream sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler">GetMediaTypeHandler</a>
</td>
<td align="left" width="63%">
Retrieves the media type handler for the stream sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker">PlaceMarker</a>
</td>
<td align="left" width="63%">
Places a marker in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample">ProcessSample</a>
</td>
<td align="left" width="63%">
Delivers a sample to the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-sinks">Media Sinks</a>
 

 

