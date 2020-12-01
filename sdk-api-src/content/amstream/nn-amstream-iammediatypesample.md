---
UID: NN:amstream.IAMMediaTypeSample
title: IAMMediaTypeSample (amstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IAMMediaTypeSample","IAMMediaTypeSample interface [DirectShow]","IAMMediaTypeSample interface [DirectShow]","described","IAMMediaTypeSampleInterface","amstream/IAMMediaTypeSample","dshow.iammediatypesample"]
old-location: dshow\iammediatypesample.htm
tech.root: dshow
ms.assetid: e0a62251-68ee-4318-b09a-0aac6b73bf54
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample, IAMMediaTypeSample interface [DirectShow], IAMMediaTypeSample interface [DirectShow],described, IAMMediaTypeSampleInterface, amstream/IAMMediaTypeSample, dshow.iammediatypesample
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAMMediaTypeSample
 - amstream/IAMMediaTypeSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample
---

# IAMMediaTypeSample interface


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
This interface contains methods for manipulating stream samples with arbitrary media types. Call the <a href="/windows/desktop/api/amstream/nf-amstream-iammediatypestream-createsample">IAMMediaTypeStream::CreateSample</a> method to create a sample that exposes this interface.

The methods in this interface parallel those of the <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface, although <b>IAMMediaTypeSample</b> contains a <a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-setpointer">SetPointer</a> method in addition to the <a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-getpointer">GetPointer</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMediaTypeSample</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>. <b>IAMMediaTypeSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMMediaTypeSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-getactualdatalength">GetActualDataLength</a>
</td>
<td align="left" width="63%">
Retrieves the data length of the sample, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-getmediatime">GetMediaTime</a>
</td>
<td align="left" width="63%">
Retrieves the media time stamps for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-getmediatype">GetMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the media type of the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-getpointer">GetPointer</a>
</td>
<td align="left" width="63%">
Retrieves a read/write pointer to the buffer's memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the buffer data area, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-gettime">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the stream times at which this sample should start and stop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-isdiscontinuity">IsDiscontinuity</a>
</td>
<td align="left" width="63%">
Determines if this sample represents a discontinuity in the data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-ispreroll">IsPreroll</a>
</td>
<td align="left" width="63%">
Determines if this sample is part of the preroll.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-issyncpoint">IsSyncPoint</a>
</td>
<td align="left" width="63%">
Determines if the beginning of a sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-setactualdatalength">SetActualDataLength</a>
</td>
<td align="left" width="63%">
Sets the sample's data length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-setdiscontinuity">SetDiscontinuity</a>
</td>
<td align="left" width="63%">
Sets the discontinuity property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-setmediatime">SetMediaTime</a>
</td>
<td align="left" width="63%">
Sets the media time stamps for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-setmediatype">SetMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-setpointer">SetPointer</a>
</td>
<td align="left" width="63%">
Sets the pointer to the media sample's memory buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-setpreroll">SetPreroll</a>
</td>
<td align="left" width="63%">
Specifies whether this is a preroll sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-setsyncpoint">SetSyncPoint</a>
</td>
<td align="left" width="63%">
Specifies whether the beginning of this sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/amstream/nf-amstream-iammediatypesample-settime">SetTime</a>
</td>
<td align="left" width="63%">
Sets the stream times at which this sample should start and stop.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>