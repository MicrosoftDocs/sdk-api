---
UID: NF:amstream.IMediaStreamFilter.ReferenceTimeToStreamTime
title: IMediaStreamFilter::ReferenceTimeToStreamTime (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The ReferenceTimeToStreamTime method converts a reference time to stream time.
helpviewer_keywords: ["IMediaStreamFilter interface [DirectShow]","ReferenceTimeToStreamTime method","IMediaStreamFilter.ReferenceTimeToStreamTime","IMediaStreamFilter::ReferenceTimeToStreamTime","IMediaStreamFilterReferenceTimeToStreamTime","ReferenceTimeToStreamTime","ReferenceTimeToStreamTime method [DirectShow]","ReferenceTimeToStreamTime method [DirectShow]","IMediaStreamFilter interface","amstream/IMediaStreamFilter::ReferenceTimeToStreamTime","dshow.imediastreamfilter_referencetimetostreamtime"]
old-location: dshow\imediastreamfilter_referencetimetostreamtime.htm
tech.root: dshow
ms.assetid: 71ddbf0b-17aa-4481-81a7-6d4a12275c31
ms.date: 12/05/2018
ms.keywords: IMediaStreamFilter interface [DirectShow],ReferenceTimeToStreamTime method, IMediaStreamFilter.ReferenceTimeToStreamTime, IMediaStreamFilter::ReferenceTimeToStreamTime, IMediaStreamFilterReferenceTimeToStreamTime, ReferenceTimeToStreamTime, ReferenceTimeToStreamTime method [DirectShow], ReferenceTimeToStreamTime method [DirectShow],IMediaStreamFilter interface, amstream/IMediaStreamFilter::ReferenceTimeToStreamTime, dshow.imediastreamfilter_referencetimetostreamtime
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
 - IMediaStreamFilter::ReferenceTimeToStreamTime
 - amstream/IMediaStreamFilter::ReferenceTimeToStreamTime
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
 - IMediaStreamFilter.ReferenceTimeToStreamTime
---

# IMediaStreamFilter::ReferenceTimeToStreamTime


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <b>ReferenceTimeToStreamTime</b> method converts a reference time to stream time.

## -parameters

### -param pTime [in, out]

On input, specifies the reference time to convert. On output, contains the equivalent stream time.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The graph does not have a reference clock.

</td>
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
</table>

## -remarks

Stream time equals the current reference time minus the reference time when the graph last started running.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter Interface</a>