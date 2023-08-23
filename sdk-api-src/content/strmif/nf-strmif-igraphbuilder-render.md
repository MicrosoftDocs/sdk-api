---
UID: NF:strmif.IGraphBuilder.Render
title: IGraphBuilder::Render (strmif.h)
description: The Render method builds a filter graph that renders the data from a specified output pin.
helpviewer_keywords: ["IGraphBuilder interface [DirectShow]","Render method","IGraphBuilder.Render","IGraphBuilder::Render","IGraphBuilderRender","Render","Render method [DirectShow]","Render method [DirectShow]","IGraphBuilder interface","dshow.igraphbuilder_render","strmif/IGraphBuilder::Render"]
old-location: dshow\igraphbuilder_render.htm
tech.root: dshow
ms.assetid: de3adac7-ff99-4415-9afc-e25ad420df59
ms.date: 4/26/2023
ms.keywords: IGraphBuilder interface [DirectShow],Render method, IGraphBuilder.Render, IGraphBuilder::Render, IGraphBuilderRender, Render, Render method [DirectShow], Render method [DirectShow],IGraphBuilder interface, dshow.igraphbuilder_render, strmif/IGraphBuilder::Render
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGraphBuilder::Render
 - strmif/IGraphBuilder::Render
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGraphBuilder.Render
---

# IGraphBuilder::Render


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Render</code> method builds a filter graph that renders the data from a specified output pin.

## -parameters

### -param ppinOut [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface on an output pin.

## -returns

Returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_AUDIO_NOT_RENDERED</b></dt>
</dl>
</td>
<td width="60%">
Partial success; the audio was not rendered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_DUPLICATE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Success; the Filter Graph Manager modified a filter name to avoid duplication.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_PARTIAL_RENDER</b></dt>
</dl>
</td>
<td width="60%">
Partial success; some of the streams in this movie are in an unsupported format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_VIDEO_NOT_RENDERED</b></dt>
</dl>
</td>
<td width="60%">
Partial success; the video was not rendered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Operation aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
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
<dt><b>VFW_E_CANNOT_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
No combination of intermediate filters could be found to make the connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CANNOT_RENDER</b></dt>
</dl>
</td>
<td width="60%">
No combination of filters could be found to render the stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_ACCEPTABLE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
There is no common media type between these pins.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_IN_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The filter to which this pin belongs is not in the filter graph.

</td>
</tr>
</table>

## -remarks

This method renders the data from a specified output pin, adding new filters to the graph as needed. Filters are tried in the same order as for the <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-connect">IGraphBuilder::Connect</a> method. For more information, see <a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>.

During the connection process, the Filter Graph Manager ignores pins on intermediate filters if the pin name begins with a tilde (~). For more information, see [PIN_INFO](/windows/desktop/api/strmif/ns-strmif-pin_info).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder Interface</a>