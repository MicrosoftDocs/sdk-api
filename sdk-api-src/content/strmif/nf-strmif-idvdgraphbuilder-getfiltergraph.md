---
UID: NF:strmif.IDvdGraphBuilder.GetFiltergraph
title: IDvdGraphBuilder::GetFiltergraph (strmif.h)
description: The GetFiltergraph method retrieves the IGraphBuilder interface for the filter graph used by the DVD-Video graph builder object.
helpviewer_keywords: ["GetFiltergraph","GetFiltergraph method [DirectShow]","GetFiltergraph method [DirectShow]","IDvdGraphBuilder interface","IDvdGraphBuilder interface [DirectShow]","GetFiltergraph method","IDvdGraphBuilder.GetFiltergraph","IDvdGraphBuilder::GetFiltergraph","IDvdGraphBuilderGetFiltergraph","dshow.idvdgraphbuilder_getfiltergraph","strmif/IDvdGraphBuilder::GetFiltergraph"]
old-location: dshow\idvdgraphbuilder_getfiltergraph.htm
tech.root: dshow
ms.assetid: 1f12140b-d10d-47d9-8bac-33fab084bff4
ms.date: 4/26/2023
ms.keywords: GetFiltergraph, GetFiltergraph method [DirectShow], GetFiltergraph method [DirectShow],IDvdGraphBuilder interface, IDvdGraphBuilder interface [DirectShow],GetFiltergraph method, IDvdGraphBuilder.GetFiltergraph, IDvdGraphBuilder::GetFiltergraph, IDvdGraphBuilderGetFiltergraph, dshow.idvdgraphbuilder_getfiltergraph, strmif/IDvdGraphBuilder::GetFiltergraph
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
 - IDvdGraphBuilder::GetFiltergraph
 - strmif/IDvdGraphBuilder::GetFiltergraph
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
 - IDvdGraphBuilder.GetFiltergraph
---

# IDvdGraphBuilder::GetFiltergraph


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetFiltergraph</code> method retrieves the <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface for the filter graph used by the DVD-Video graph builder object.

## -parameters

### -param ppGB [out]

Address of a pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface that the DVD-Video graph builder object is using.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The current DirectShow implementation returns E_INVALIDARG if <i>ppGB</i> is invalid.

## -remarks

The returned <b>IGraphBuilder</b> interface pointer has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdgraphbuilder">IDvdGraphBuilder Interface</a>