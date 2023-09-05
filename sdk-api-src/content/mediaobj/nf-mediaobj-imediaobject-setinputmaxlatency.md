---
UID: NF:mediaobj.IMediaObject.SetInputMaxLatency
title: IMediaObject::SetInputMaxLatency (mediaobj.h)
description: The SetInputMaxLatency method sets the maximum latency on a specified input stream. For the definition of maximum latency, see IMediaObject::GetInputMaxLatency.
helpviewer_keywords: ["IMediaObject interface [DirectShow]","SetInputMaxLatency method","IMediaObject.SetInputMaxLatency","IMediaObject::SetInputMaxLatency","IMediaObjectSetInputMaxLatency","SetInputMaxLatency","SetInputMaxLatency method [DirectShow]","SetInputMaxLatency method [DirectShow]","IMediaObject interface","dshow.imediaobject_setinputmaxlatency","mediaobj/IMediaObject::SetInputMaxLatency"]
old-location: dshow\imediaobject_setinputmaxlatency.htm
tech.root: dshow
ms.assetid: 45fb0caa-cd12-4847-a646-f6fd90c50b81
ms.date: 4/26/2023
ms.keywords: IMediaObject interface [DirectShow],SetInputMaxLatency method, IMediaObject.SetInputMaxLatency, IMediaObject::SetInputMaxLatency, IMediaObjectSetInputMaxLatency, SetInputMaxLatency, SetInputMaxLatency method [DirectShow], SetInputMaxLatency method [DirectShow],IMediaObject interface, dshow.imediaobject_setinputmaxlatency, mediaobj/IMediaObject::SetInputMaxLatency
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
 - IMediaObject::SetInputMaxLatency
 - mediaobj/IMediaObject::SetInputMaxLatency
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
 - IMediaObject.SetInputMaxLatency
---

# IMediaObject::SetInputMaxLatency


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetInputMaxLatency</code> method sets the maximum latency on a specified input stream. For the definition of maximum latency, see <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency">IMediaObject::GetInputMaxLatency</a>.

## -parameters

### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.

### -param rtMaxLatency

Maximum latency.

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
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>



<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency">IMediaObject::GetInputMaxLatency</a>