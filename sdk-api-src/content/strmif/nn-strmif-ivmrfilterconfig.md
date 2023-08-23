---
UID: NN:strmif.IVMRFilterConfig
title: IVMRFilterConfig (strmif.h)
description: The IVMRFilterConfig interface is used to configure the operating mode and video rendering mechanisms of the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRFilterConfig","IVMRFilterConfig interface [DirectShow]","IVMRFilterConfig interface [DirectShow]","described","IVMRFilterConfigInterface","dshow.ivmrfilterconfig","strmif/IVMRFilterConfig"]
old-location: dshow\ivmrfilterconfig.htm
tech.root: dshow
ms.assetid: 3ea7bb41-1f5f-496f-bdf4-776ec9f28876
ms.date: 4/26/2023
ms.keywords: IVMRFilterConfig, IVMRFilterConfig interface [DirectShow], IVMRFilterConfig interface [DirectShow],described, IVMRFilterConfigInterface, dshow.ivmrfilterconfig, strmif/IVMRFilterConfig
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVMRFilterConfig
 - strmif/IVMRFilterConfig
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
 - IVMRFilterConfig
---

# IVMRFilterConfig interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRFilterConfig</code> interface is used to configure the operating mode and video rendering mechanisms of the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). For the VMR-9, use the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9</a> interface.

Applications must add the VMR to the graph and configure it before connecting it to any upstream filters (for example, in a call to <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>). Once a filter has been connected to the VMR, the VMR's configuration is locked and all future attempts to alter it fail.

## -inheritance

The <b>IVMRFilterConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRFilterConfig</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
