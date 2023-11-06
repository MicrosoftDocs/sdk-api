---
UID: NF:mediaobj.IMediaObject.GetInputStatus
title: IMediaObject::GetInputStatus (mediaobj.h)
description: The GetInputStatus method queries whether an input stream can accept more input data.
helpviewer_keywords: ["GetInputStatus","GetInputStatus method [DirectShow]","GetInputStatus method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","GetInputStatus method","IMediaObject.GetInputStatus","IMediaObject::GetInputStatus","IMediaObjectGetInputStatus","dshow.imediaobject_getinputstatus","mediaobj/IMediaObject::GetInputStatus"]
old-location: dshow\imediaobject_getinputstatus.htm
tech.root: dshow
ms.assetid: 4581307f-cea2-4e88-81a1-972e1998c7a8
ms.date: 4/26/2023
ms.keywords: GetInputStatus, GetInputStatus method [DirectShow], GetInputStatus method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetInputStatus method, IMediaObject.GetInputStatus, IMediaObject::GetInputStatus, IMediaObjectGetInputStatus, dshow.imediaobject_getinputstatus, mediaobj/IMediaObject::GetInputStatus
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
 - IMediaObject::GetInputStatus
 - mediaobj/IMediaObject::GetInputStatus
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
 - IMediaObject.GetInputStatus
---

# IMediaObject::GetInputStatus


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetInputStatus</code> method queries whether an input stream can accept more input data.

## -parameters

### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.

### -param dwFlags [out]

Pointer to a variable that receives either zero or DMO_INPUT_STATUSF_ACCEPT_DATA.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

If the input stream will accept more data, the method returns the DMO_INPUT_STATUSF_ACCEPT_DATA flag in the <i>dwFlags</i> parameter. Otherwise, it sets this parameter to zero. If the stream will accept more data, the application can call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput">IMediaObject::ProcessInput</a> method.

The status of an input stream can change only as the result of one of the following method calls.

<table>
<tr>
<th>Method
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity">IMediaObject::Discontinuity</a>
</td>
<td>Signals a discontinuity on the specified input stream.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush">IMediaObject::Flush</a>
</td>
<td>Flushes all internally buffered data.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput">IMediaObject::ProcessInput</a>
</td>
<td>Delivers a buffer to the specified input stream.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">IMediaObject::ProcessOutput</a>
</td>
<td>Generates output from the current input data.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>