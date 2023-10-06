---
UID: NF:strmif.IFilterGraph.ConnectDirect
title: IFilterGraph::ConnectDirect (strmif.h)
description: The ConnectDirect method connects the two pins directly (without intervening filters).
helpviewer_keywords: ["ConnectDirect","ConnectDirect method [DirectShow]","ConnectDirect method [DirectShow]","IFilterGraph interface","IFilterGraph interface [DirectShow]","ConnectDirect method","IFilterGraph.ConnectDirect","IFilterGraph::ConnectDirect","IFilterGraphConnectDirect","dshow.ifiltergraph_connectdirect","strmif/IFilterGraph::ConnectDirect"]
old-location: dshow\ifiltergraph_connectdirect.htm
tech.root: dshow
ms.assetid: fb17bd98-dd6b-4fad-9b56-9cab10725b28
ms.date: 4/26/2023
ms.keywords: ConnectDirect, ConnectDirect method [DirectShow], ConnectDirect method [DirectShow],IFilterGraph interface, IFilterGraph interface [DirectShow],ConnectDirect method, IFilterGraph.ConnectDirect, IFilterGraph::ConnectDirect, IFilterGraphConnectDirect, dshow.ifiltergraph_connectdirect, strmif/IFilterGraph::ConnectDirect
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
 - IFilterGraph::ConnectDirect
 - strmif/IFilterGraph::ConnectDirect
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
 - IFilterGraph.ConnectDirect
---

# IFilterGraph::ConnectDirect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ConnectDirect</code> method connects the two pins directly (without intervening filters).

## -parameters

### -param ppinOut [in]

Pointer to the output pin.

### -param ppinIn [in]

Pointer to the input pin.

### -param pmt [in]

Pointer to the media type to use for the connection (optional; can be <b>NULL</b>).

## -returns

Returns one of the following values, or an error value returned by <a href="/windows/desktop/api/strmif/nf-strmif-ipin-connect">IPin::Connect</a>.

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
<dt><b>VFW_E_NOT_IN_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
One of the specified pins is not in the graph.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CIRCULAR_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The input pin is upstream of the output pin, which would result in a circular graph.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph Interface</a>