---
UID: NN:strmif.ICaptureGraphBuilder2
title: ICaptureGraphBuilder2 (strmif.h)
description: The ICaptureGraphBuilder2 interface builds capture graphs and other custom filter graphs.
helpviewer_keywords: ["ICaptureGraphBuilder2","ICaptureGraphBuilder2 interface [DirectShow]","ICaptureGraphBuilder2 interface [DirectShow]","described","ICaptureGraphBuilder2Interface","dshow.icapturegraphbuilder2","strmif/ICaptureGraphBuilder2"]
old-location: dshow\icapturegraphbuilder2.htm
tech.root: dshow
ms.assetid: abdf6fb2-e98f-4df8-98ec-06d33798abb5
ms.date: 4/26/2023
ms.keywords: ICaptureGraphBuilder2, ICaptureGraphBuilder2 interface [DirectShow], ICaptureGraphBuilder2 interface [DirectShow],described, ICaptureGraphBuilder2Interface, dshow.icapturegraphbuilder2, strmif/ICaptureGraphBuilder2
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
 - ICaptureGraphBuilder2
 - strmif/ICaptureGraphBuilder2
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
 - ICaptureGraphBuilder2
---

# ICaptureGraphBuilder2 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ICaptureGraphBuilder2</code> interface builds capture graphs and other custom filter graphs. The <a href="/windows/desktop/DirectShow/capture-graph-builder">Capture Graph Builder</a> object implements this interface.

<div class="alert"><b>Note</b>  By default, the <code>ICaptureGraphBuilder2</code> interface does not use the Video Mixing Renderer (VMR), Enhanced Video Renderer (EVR) or <a href="/windows/desktop/DirectShow/video-port-manager">Video Port Manager</a> filters.</div>
<div> </div>

## -inheritance

The <b>ICaptureGraphBuilder2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICaptureGraphBuilder2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/building-graphs-with-the-capture-graph-builder">Building Graphs with the Capture Graph Builder</a>



<a href="/windows/desktop/DirectShow/recompressing-an-avi-file">Recompressing an AVI File</a>



<a href="/windows/desktop/DirectShow/video-capture">Video Capture</a>
