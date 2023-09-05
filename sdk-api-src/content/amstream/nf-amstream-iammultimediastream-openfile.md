---
UID: NF:amstream.IAMMultiMediaStream.OpenFile
title: IAMMultiMediaStream::OpenFile (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The OpenFile method opens and automatically creates a filter graph for the specified media file. If DirectShow doesn't support the file format, this method does nothing.
helpviewer_keywords: ["IAMMultiMediaStream interface [DirectShow]","OpenFile method","IAMMultiMediaStream.OpenFile","IAMMultiMediaStream::OpenFile","IAMMultiMediaStreamOpenFile","OpenFile","OpenFile method [DirectShow]","OpenFile method [DirectShow]","IAMMultiMediaStream interface","amstream/IAMMultiMediaStream::OpenFile","dshow.iammultimediastream_openfile"]
old-location: dshow\iammultimediastream_openfile.htm
tech.root: dshow
ms.assetid: 0b3f7401-9afe-41e5-827f-e4e8d60b7480
ms.date: 4/26/2023
ms.keywords: IAMMultiMediaStream interface [DirectShow],OpenFile method, IAMMultiMediaStream.OpenFile, IAMMultiMediaStream::OpenFile, IAMMultiMediaStreamOpenFile, OpenFile, OpenFile method [DirectShow], OpenFile method [DirectShow],IAMMultiMediaStream interface, amstream/IAMMultiMediaStream::OpenFile, dshow.iammultimediastream_openfile
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
 - IAMMultiMediaStream::OpenFile
 - amstream/IAMMultiMediaStream::OpenFile
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
 - IAMMultiMediaStream.OpenFile
---

# IAMMultiMediaStream::OpenFile


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>OpenFile</code> method opens and automatically creates a filter graph for the specified media file. If DirectShow doesn't support the file format, this method does nothing.

## -parameters

### -param pszFileName [in]

Pointer to the name of the file you want to open.

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

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
This method tried to access an invalid pointer.

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

The AMMSF_RENDERALLSTREAMS flag will create default rendering filters for video and audio if they do not exist. However, these default filters cannot be accessed by the <a href="/windows/desktop/api/mmstream/nf-mmstream-istreamsample-getmediastream">IStreamSample::GetMediaStream</a> method.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream Interface</a>