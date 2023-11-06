---
UID: NN:strmif.IGraphBuilder
title: IGraphBuilder (strmif.h)
description: This interface provides methods that enable an application to build a filter graph.
helpviewer_keywords: ["IGraphBuilder","IGraphBuilder interface [DirectShow]","IGraphBuilder interface [DirectShow]","described","IGraphBuilderInterface","dshow.igraphbuilder","strmif/IGraphBuilder"]
old-location: dshow\igraphbuilder.htm
tech.root: dshow
ms.assetid: 54ed8ac8-4821-4c0c-9fb9-789c70dbca37
ms.date: 4/26/2023
ms.keywords: IGraphBuilder, IGraphBuilder interface [DirectShow], IGraphBuilder interface [DirectShow],described, IGraphBuilderInterface, dshow.igraphbuilder, strmif/IGraphBuilder
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
 - IGraphBuilder
 - strmif/IGraphBuilder
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
 - IGraphBuilder
---

# IGraphBuilder interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This interface provides methods that enable an application to build a filter graph. The <a href="/windows/desktop/DirectShow/filter-graph-manager">Filter Graph Manager</a> implements this interface.

The <b>IGraphBuilder</b> interface inherits from the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> interface. <b>IFilterGraph</b> provides basic operations, such as adding a filter to the graph or connecting two pins. <b>IGraphBuilder</b> adds further methods that construct graphs from partial information. For example, the <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a> method builds a graph for file playback, given the name of the file. The <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">IGraphBuilder::Render</a> method renders data from an output pin by connecting new filters to the pin.

Using these methods, an application does not need to specify every filter and pin connection in the graph. Instead, the Filter Graph Manager selects filters that are registered on the user's system, adds them to the graph, and connects them. For more information, see <a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>.

## -inheritance

The <b>IGraphBuilder</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a>. <b>IGraphBuilder</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a>



<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
