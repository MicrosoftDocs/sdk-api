---
UID: NF:mediaobj.IMediaObject.Discontinuity
title: IMediaObject::Discontinuity (mediaobj.h)
description: The Discontinuity method signals a discontinuity on the specified input stream.
helpviewer_keywords: ["Discontinuity","Discontinuity method [DirectShow]","Discontinuity method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","Discontinuity method","IMediaObject.Discontinuity","IMediaObject::Discontinuity","IMediaObjectDiscontinuity","dshow.imediaobject_discontinuity","mediaobj/IMediaObject::Discontinuity"]
old-location: dshow\imediaobject_discontinuity.htm
tech.root: dshow
ms.assetid: 1a8e51e2-5d19-423d-acd2-8f1c0a143cf3
ms.date: 4/26/2023
ms.keywords: Discontinuity, Discontinuity method [DirectShow], Discontinuity method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],Discontinuity method, IMediaObject.Discontinuity, IMediaObject::Discontinuity, IMediaObjectDiscontinuity, dshow.imediaobject_discontinuity, mediaobj/IMediaObject::Discontinuity
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
 - IMediaObject::Discontinuity
 - mediaobj/IMediaObject::Discontinuity
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
 - IMediaObject.Discontinuity
---

# IMediaObject::Discontinuity


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Discontinuity</code> method signals a discontinuity on the specified input stream.

## -parameters

### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.

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
<dt><b>DMO_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
The DMO is not accepting input.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The input and output types have not been set.

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

## -remarks

A discontinuity represents a break in the input. A discontinuity might occur because no more data is expected, the format is changing, or there is a gap in the data. After a discontinuity, the DMO does not accept further input on that stream until all pending data has been processed. The application should call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">IMediaObject::ProcessOutput</a> method until none of the streams returns the DMO_OUTPUT_DATA_BUFFERF_INCOMPLETE flag.

This method might fail if it is called before the client sets the input and output types on the DMO.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>