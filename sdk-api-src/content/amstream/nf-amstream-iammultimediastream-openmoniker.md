---
UID: NF:amstream.IAMMultiMediaStream.OpenMoniker
title: IAMMultiMediaStream::OpenMoniker (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The OpenMoniker method opens a file or device moniker; you can read media data from this moniker if DirectShow supports the moniker.
helpviewer_keywords: ["IAMMultiMediaStream interface [DirectShow]","OpenMoniker method","IAMMultiMediaStream.OpenMoniker","IAMMultiMediaStream::OpenMoniker","IAMMultiMediaStreamOpenMoniker","OpenMoniker","OpenMoniker method [DirectShow]","OpenMoniker method [DirectShow]","IAMMultiMediaStream interface","amstream/IAMMultiMediaStream::OpenMoniker","dshow.iammultimediastream_openmoniker"]
old-location: dshow\iammultimediastream_openmoniker.htm
tech.root: dshow
ms.assetid: ccfed197-6637-4283-9996-56049da49b84
ms.date: 4/26/2023
ms.keywords: IAMMultiMediaStream interface [DirectShow],OpenMoniker method, IAMMultiMediaStream.OpenMoniker, IAMMultiMediaStream::OpenMoniker, IAMMultiMediaStreamOpenMoniker, OpenMoniker, OpenMoniker method [DirectShow], OpenMoniker method [DirectShow],IAMMultiMediaStream interface, amstream/IAMMultiMediaStream::OpenMoniker, dshow.iammultimediastream_openmoniker
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
 - IAMMultiMediaStream::OpenMoniker
 - amstream/IAMMultiMediaStream::OpenMoniker
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
 - IAMMultiMediaStream.OpenMoniker
---

# IAMMultiMediaStream::OpenMoniker


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>OpenMoniker</code> method opens a file or device moniker; you can read media data from this moniker if DirectShow supports the moniker.

## -parameters

### -param pCtx [in]

Pointer to the bind context associated with the moniker.

### -param pMoniker [in]

Pointer to an <b>IMoniker</b> interface that specifies the moniker you want to open.

### -param dwFlags [in]

Value that modifies how the filter graph will render the specified file. This value is a combination of one or more of the following flags.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AMMSF_NOCLOCK</td>
<td>Run the stream with no clock.</td>
</tr>
<tr>
<td>AMMSF_NORENDER</td>
<td>Open the file, but do not render any streams. This flag should always be accompanied with the AMMSF_RUN flag.</td>
</tr>
<tr>
<td>AMMSF_RENDERALLSTREAMS</td>
<td>Render all streams, including those that do not have an existing media stream.</td>
</tr>
<tr>
<td>AMMSF_RENDERTOEXISTING</td>
<td>Only render to existing streams.</td>
</tr>
<tr>
<td>AMMSF_RUN</td>
<td>Set the stream into the run state.</td>
</tr>
</table>

## -returns

Returns S_OK if successful or E_INVALIDARG if the <i>dwFlags</i> parameter is invalid.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream Interface</a>