---
UID: NF:strmif.ICaptureGraphBuilder.GetFiltergraph
title: ICaptureGraphBuilder::GetFiltergraph (strmif.h)
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Retrieves the filter graph that the builder is using.
helpviewer_keywords: ["GetFiltergraph","GetFiltergraph method [DirectShow]","GetFiltergraph method [DirectShow]","ICaptureGraphBuilder interface","ICaptureGraphBuilder interface [DirectShow]","GetFiltergraph method","ICaptureGraphBuilder.GetFiltergraph","ICaptureGraphBuilder::GetFiltergraph","ICaptureGraphBuilderGetFiltergraph","dshow.icapturegraphbuilder_getfiltergraph","strmif/ICaptureGraphBuilder::GetFiltergraph"]
old-location: dshow\icapturegraphbuilder_getfiltergraph.htm
tech.root: dshow
ms.assetid: 9cb43dca-79f1-4467-8e17-6f2a0b4db785
ms.date: 4/26/2023
ms.keywords: GetFiltergraph, GetFiltergraph method [DirectShow], GetFiltergraph method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],GetFiltergraph method, ICaptureGraphBuilder.GetFiltergraph, ICaptureGraphBuilder::GetFiltergraph, ICaptureGraphBuilderGetFiltergraph, dshow.icapturegraphbuilder_getfiltergraph, strmif/ICaptureGraphBuilder::GetFiltergraph
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
 - ICaptureGraphBuilder::GetFiltergraph
 - strmif/ICaptureGraphBuilder::GetFiltergraph
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
 - ICaptureGraphBuilder.GetFiltergraph
---

# ICaptureGraphBuilder::GetFiltergraph


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Retrieves the filter graph that the builder is using.

## -parameters

### -param ppfg [out]

Address of a pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method increments the reference count on the <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface; be sure to decrement the reference count on <b>IGraphBuilder</b> by calling the <b>Release</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder">ICaptureGraphBuilder Interface</a>