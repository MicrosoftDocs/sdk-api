---
UID: NN:strmif.IMediaSample
title: IMediaSample (strmif.h)
author: windows-sdk-content
description: The IMediaSample interface sets and retrieves properties on media samples.
old-location: dshow\imediasample.htm
tech.root: DirectShow
ms.assetid: 883e5e3b-db91-4806-96cc-c6f8cddfcca6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaSample, IMediaSample interface [DirectShow], IMediaSample interface [DirectShow],described, IMediaSampleInterface, dshow.imediasample, strmif/IMediaSample
ms.topic: interface
f1_keywords: 
 - "strmif/IMediaSample"
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSample interface


## -description



The <code>IMediaSample</code> interface sets and retrieves properties on media samples. A media sample is a COM object that contains a block of media data. Media samples support the use of shared memory buffers among filters.

Typically, applications do not call methods on this interface. Filters use this interface to set properties on samples, and deliver the samples to a downstream filter. The downstream filter uses the interface to retrieve the properties and read the data. The filter can modify the data in place, or it can copy the sample, modify the copy, and pass the copy downstream.

The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediasample2">IMediaSample2</a> interface inherits this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaSample</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-getactualdatalength">GetActualDataLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the valid data in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-getmediatime">GetMediaTime</a>
</td>
<td align="left" width="63%">
Retrieves the media times for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-getmediatype">GetMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the media type, if the media type differs from the previous sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-getpointer">GetPointer</a>
</td>
<td align="left" width="63%">
Retrieves a read/write pointer to this buffer's memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-gettime">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the stream times at which this sample should begin and finish.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-isdiscontinuity">IsDiscontinuity</a>
</td>
<td align="left" width="63%">
Determines if this sample represents a break in the data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-ispreroll">IsPreroll</a>
</td>
<td align="left" width="63%">
Determines if this sample is a preroll sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-issyncpoint">IsSyncPoint</a>
</td>
<td align="left" width="63%">
Determines if the beginning of this sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-setactualdatalength">SetActualDataLength</a>
</td>
<td align="left" width="63%">
Sets the length of the valid data in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-setdiscontinuity">SetDiscontinuity</a>
</td>
<td align="left" width="63%">
Specifies whether this sample represents a break in the data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-setmediatime">SetMediaTime</a>
</td>
<td align="left" width="63%">
Sets the media times for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-setmediatype">SetMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-setpreroll">SetPreroll</a>
</td>
<td align="left" width="63%">
Specifies whether this sample is a preroll sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-setsyncpoint">SetSyncPoint</a>
</td>
<td align="left" width="63%">
Specifies whether the beginning of this sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-settime">SetTime</a>
</td>
<td align="left" width="63%">
Sets the stream time when this sample should begin and finish.

</td>
</tr>
</table> 

