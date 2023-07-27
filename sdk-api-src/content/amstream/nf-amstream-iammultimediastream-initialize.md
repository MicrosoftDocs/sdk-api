---
UID: NF:amstream.IAMMultiMediaStream.Initialize
title: IAMMultiMediaStream::Initialize (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The Initialize method initializes the multimedia stream object.
helpviewer_keywords: ["IAMMultiMediaStream interface [DirectShow]","Initialize method","IAMMultiMediaStream.Initialize","IAMMultiMediaStream::Initialize","IAMMultiMediaStreamInitialize","Initialize","Initialize method [DirectShow]","Initialize method [DirectShow]","IAMMultiMediaStream interface","amstream/IAMMultiMediaStream::Initialize","dshow.iammultimediastream_initialize"]
old-location: dshow\iammultimediastream_initialize.htm
tech.root: dshow
ms.assetid: c9c3295e-716f-4093-b437-f6c405f5bc7b
ms.date: 4/26/2023
ms.keywords: IAMMultiMediaStream interface [DirectShow],Initialize method, IAMMultiMediaStream.Initialize, IAMMultiMediaStream::Initialize, IAMMultiMediaStreamInitialize, Initialize, Initialize method [DirectShow], Initialize method [DirectShow],IAMMultiMediaStream interface, amstream/IAMMultiMediaStream::Initialize, dshow.iammultimediastream_initialize
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
 - IAMMultiMediaStream::Initialize
 - amstream/IAMMultiMediaStream::Initialize
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
 - IAMMultiMediaStream.Initialize
---

# IAMMultiMediaStream::Initialize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>Initialize</code> method initializes the multimedia stream object.

## -parameters

### -param StreamType [in]

Member of the <a href="/previous-versions/windows/desktop/api/mmstream/ne-mmstream-stream_type">STREAM_TYPE</a> enumeration, specifying whether the streams are read-only, write-only, or read/write.

### -param dwFlags [in]

Must be one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>Create a filter graph that runs on a separate thread.</td>
</tr>
<tr>
<td>AMMSF_NOGRAPHTHREAD</td>
<td>Create a filter graph that runs on the calling thread.</td>
</tr>
</table>

### -param pFilterGraph [in]

[optional] Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface, or <b>NULL</b>. If this parameter is non-<b>NULL</b>, it specifies a filter graph that the multimedia stream object will use. Otherwise, the multimedia stream object creates a new filter graph.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

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

If you specify AMMSF_NOGRAPHTHREAD in the <i>dwFlags</i> parameter, the calling thread must process window messages, and it must release all multimedia streaming objects before the thread exits. Otherwise, the application might deadlock.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream Interface</a>