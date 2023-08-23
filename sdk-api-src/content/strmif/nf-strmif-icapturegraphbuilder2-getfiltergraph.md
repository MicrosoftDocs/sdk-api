---
UID: NF:strmif.ICaptureGraphBuilder2.GetFiltergraph
title: ICaptureGraphBuilder2::GetFiltergraph (strmif.h)
description: The GetFiltergraph method retrieves the filter graph that the capture graph builder is using.
helpviewer_keywords: ["GetFiltergraph","GetFiltergraph method [DirectShow]","GetFiltergraph method [DirectShow]","ICaptureGraphBuilder2 interface","ICaptureGraphBuilder2 interface [DirectShow]","GetFiltergraph method","ICaptureGraphBuilder2.GetFiltergraph","ICaptureGraphBuilder2::GetFiltergraph","ICaptureGraphBuilder2GetFiltergraph","dshow.icapturegraphbuilder2_getfiltergraph","strmif/ICaptureGraphBuilder2::GetFiltergraph"]
old-location: dshow\icapturegraphbuilder2_getfiltergraph.htm
tech.root: dshow
ms.assetid: 91136a71-cfda-4aa5-ba6c-d1ce6cbef3c1
ms.date: 4/26/2023
ms.keywords: GetFiltergraph, GetFiltergraph method [DirectShow], GetFiltergraph method [DirectShow],ICaptureGraphBuilder2 interface, ICaptureGraphBuilder2 interface [DirectShow],GetFiltergraph method, ICaptureGraphBuilder2.GetFiltergraph, ICaptureGraphBuilder2::GetFiltergraph, ICaptureGraphBuilder2GetFiltergraph, dshow.icapturegraphbuilder2_getfiltergraph, strmif/ICaptureGraphBuilder2::GetFiltergraph
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
 - ICaptureGraphBuilder2::GetFiltergraph
 - strmif/ICaptureGraphBuilder2::GetFiltergraph
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
 - ICaptureGraphBuilder2.GetFiltergraph
---

# ICaptureGraphBuilder2::GetFiltergraph


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetFiltergraph</code> method retrieves the filter graph that the capture graph builder is using.

## -parameters

### -param ppfg [out]

Receives an <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface pointer.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No filter graph.

</td>
</tr>
</table>

## -remarks

Initially, the capture graph builder does not hold a pointer to a filter graph. This method returns E_UNEXPECTED until one of the following methods has been called:

<ul>
<li>
<a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-renderstream">ICaptureGraphBuilder2::RenderStream</a>
</li>
<li>
<a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph">ICaptureGraphBuilder2::SetFiltergraph</a>
</li>
<li>
<a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename">ICaptureGraphBuilder2::SetOutputFileName</a>
</li>
</ul>
This method increments the reference count on the <b>IGraphBuilder</b> interface. Be sure to release the interface when you are done with it.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2 Interface</a>