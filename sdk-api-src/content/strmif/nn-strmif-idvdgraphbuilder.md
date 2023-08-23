---
UID: NN:strmif.IDvdGraphBuilder
title: IDvdGraphBuilder (strmif.h)
description: The IDvdGraphBuilder interface builds a filter graph for DVD-Video playback.
helpviewer_keywords: ["IDvdGraphBuilder","IDvdGraphBuilder interface [DirectShow]","IDvdGraphBuilder interface [DirectShow]","described","IDvdGraphBuilderInterface","dshow.idvdgraphbuilder","strmif/IDvdGraphBuilder"]
old-location: dshow\idvdgraphbuilder.htm
tech.root: dshow
ms.assetid: 2179e54a-c6e2-4837-9f89-be210bde9180
ms.date: 4/26/2023
ms.keywords: IDvdGraphBuilder, IDvdGraphBuilder interface [DirectShow], IDvdGraphBuilder interface [DirectShow],described, IDvdGraphBuilderInterface, dshow.idvdgraphbuilder, strmif/IDvdGraphBuilder
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
 - IDvdGraphBuilder
 - strmif/IDvdGraphBuilder
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
 - IDvdGraphBuilder
---

# IDvdGraphBuilder interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDvdGraphBuilder</code> interface builds a filter graph for DVD-Video playback. The <a href="/windows/desktop/DirectShow/dvd-graph-builder">DVD Graph Builder</a> object implements this interface.

The <a href="/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">RenderDvdVideoVolume</a> method builds a DVD playback graph from the available software and hardware on the system. For information on how to build the DVD filter graph and obtain the pointers to all the necessary interfaces, see <a href="/windows/desktop/DirectShow/building-the-dvd-filter-graph">Building the DVD Filter Graph</a>.

<div class="alert"><b>Note</b>  A DVD filter graph requires either a hardware or software MPEG-2 decoder.</div>
<div> </div>
Generally, you should not add, remove, connect, disconnect, or access individual filters in the graph created by <b>RenderDvdVideoVolume</b>, because doing so might confuse the cleanup code. The purpose of the <b>DvdGraphBuilder</b> object is to simplify the development of DVD-Video applications. If you need a specific type of graph for a particular solution, you should manually create the entire filter graph.

## -inheritance

The <b>IDvdGraphBuilder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdGraphBuilder</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>
