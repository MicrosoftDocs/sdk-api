---
UID: NN:strmif.IFilterGraph
title: IFilterGraph (strmif.h)
description: The IFilterGraph interface provides methods for building a filter graph.
helpviewer_keywords: ["IFilterGraph","IFilterGraph interface [DirectShow]","IFilterGraph interface [DirectShow]","described","IFilterGraphInterface","dshow.ifiltergraph","strmif/IFilterGraph"]
old-location: dshow\ifiltergraph.htm
tech.root: dshow
ms.assetid: 73a92f44-03c6-47e3-98d1-a20100ed8fa1
ms.date: 4/26/2023
ms.keywords: IFilterGraph, IFilterGraph interface [DirectShow], IFilterGraph interface [DirectShow],described, IFilterGraphInterface, dshow.ifiltergraph, strmif/IFilterGraph
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
 - IFilterGraph
 - strmif/IFilterGraph
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
 - IFilterGraph
---

# IFilterGraph interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IFilterGraph</code> interface provides methods for building a filter graph. An application can use it to add filters to the graph, connect or disconnect filters, remove filters, and perform other basic operations. However, the <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface inherits from this interface and provides additional methods that are more sophisticated. Therefore, applications should use <b>IGraphBuilder</b> rather than using <code>IFilterGraph</code> directly.

The filter graph manager implements this interface.

## -inheritance

The <b>IFilterGraph</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFilterGraph</b> also has these types of members:

