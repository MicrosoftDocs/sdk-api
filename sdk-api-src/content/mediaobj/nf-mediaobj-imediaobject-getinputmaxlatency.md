---
UID: NF:mediaobj.IMediaObject.GetInputMaxLatency
title: IMediaObject::GetInputMaxLatency (mediaobj.h)
description: The GetInputMaxLatency method retrieves the maximum latency on a specified input stream.
helpviewer_keywords: ["GetInputMaxLatency","GetInputMaxLatency method [DirectShow]","GetInputMaxLatency method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","GetInputMaxLatency method","IMediaObject.GetInputMaxLatency","IMediaObject::GetInputMaxLatency","IMediaObjectGetInputMaxLatency","dshow.imediaobject_getinputmaxlatency","mediaobj/IMediaObject::GetInputMaxLatency"]
old-location: dshow\imediaobject_getinputmaxlatency.htm
tech.root: dshow
ms.assetid: f8a18b4c-a59c-4e9d-aff7-62333e9ffda9
ms.date: 12/05/2018
ms.keywords: GetInputMaxLatency, GetInputMaxLatency method [DirectShow], GetInputMaxLatency method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetInputMaxLatency method, IMediaObject.GetInputMaxLatency, IMediaObject::GetInputMaxLatency, IMediaObjectGetInputMaxLatency, dshow.imediaobject_getinputmaxlatency, mediaobj/IMediaObject::GetInputMaxLatency
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObject::GetInputMaxLatency
 - mediaobj/IMediaObject::GetInputMaxLatency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.GetInputMaxLatency
---

# IMediaObject::GetInputMaxLatency


## -description

The <code>GetInputMaxLatency</code> method retrieves the maximum latency on a specified input stream.

## -parameters

### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.

### -param prtMaxLatency [out]

Pointer to a variable that receives the maximum latency.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. Assume zero latency.

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

The latency is the difference between a time stamp on the input stream and the corresponding time stamp on the output stream. The maximum latency is the largest possible difference in the time stamps. For a DMO, determine the maximum latency as follows:

<ul>
<li>Process input buffers until the DMO can produce output. </li>
<li>Process as many output buffers as possible. </li>
<li>The maximum latency is the largest delta between input time stamps and output time stamps (taken as an absolute value). </li>
</ul>
Under this definition, latency does not include the time that it takes to process samples. Nor does it include any latency introduced by the size of the input buffer.

For the special case where a DMO processes exactly one sample at a time, the maximum latency is simply the difference in time stamps.

Latency is defined only when samples have time stamps, and the time stamps increase or decrease monotonically. Maximum latency might depend on the media types for the input and output streams.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>