---
UID: NF:strmif.ICaptureGraphBuilder.SetFiltergraph
title: ICaptureGraphBuilder::SetFiltergraph (strmif.h)
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Tells the graph builder object which filter graph to use.
helpviewer_keywords: ["ICaptureGraphBuilder interface [DirectShow]","SetFiltergraph method","ICaptureGraphBuilder.SetFiltergraph","ICaptureGraphBuilder::SetFiltergraph","ICaptureGraphBuilderSetFiltergraph","SetFiltergraph","SetFiltergraph method [DirectShow]","SetFiltergraph method [DirectShow]","ICaptureGraphBuilder interface","dshow.icapturegraphbuilder_setfiltergraph","strmif/ICaptureGraphBuilder::SetFiltergraph"]
old-location: dshow\icapturegraphbuilder_setfiltergraph.htm
tech.root: dshow
ms.assetid: 01cb7f09-6ff2-46c1-b6f2-76583785b242
ms.date: 4/26/2023
ms.keywords: ICaptureGraphBuilder interface [DirectShow],SetFiltergraph method, ICaptureGraphBuilder.SetFiltergraph, ICaptureGraphBuilder::SetFiltergraph, ICaptureGraphBuilderSetFiltergraph, SetFiltergraph, SetFiltergraph method [DirectShow], SetFiltergraph method [DirectShow],ICaptureGraphBuilder interface, dshow.icapturegraphbuilder_setfiltergraph, strmif/ICaptureGraphBuilder::SetFiltergraph
req.header: strmif.h
req.include-header: Dshow.h
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
 - ICaptureGraphBuilder::SetFiltergraph
 - strmif/ICaptureGraphBuilder::SetFiltergraph
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - ICaptureGraphBuilder.SetFiltergraph
---

# ICaptureGraphBuilder::SetFiltergraph


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Tells the graph builder object which filter graph to use.

## -parameters

### -param pfg [in]

Pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface that specifies the filter graph to use for subsequent calls to the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-addfilter">IFilterGraph::AddFilter</a> method.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The graph builder will automatically create a filter graph if you don't call this method. If you call this method after the graph builder has created its own filter graph, the call will fail.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder">ICaptureGraphBuilder Interface</a>