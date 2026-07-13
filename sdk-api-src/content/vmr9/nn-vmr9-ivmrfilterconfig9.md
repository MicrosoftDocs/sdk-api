---
UID: NN:vmr9.IVMRFilterConfig9
title: IVMRFilterConfig9 (vmr9.h)
description: The IVMRFilterConfig9 interface is implemented by the Video Mixing Renderer Filter 9.
helpviewer_keywords: ["IVMRFilterConfig9","IVMRFilterConfig9 interface [DirectShow]","IVMRFilterConfig9 interface [DirectShow]","described","IVMRFilterConfig9Interface","dshow.ivmrfilterconfig9","vmr9/IVMRFilterConfig9"]
old-location: dshow\ivmrfilterconfig9.htm
tech.root: dshow
ms.assetid: 089e44c8-6a27-410d-aad5-08816bd4f915
ms.date: 4/26/2023
ms.keywords: IVMRFilterConfig9, IVMRFilterConfig9 interface [DirectShow], IVMRFilterConfig9 interface [DirectShow],described, IVMRFilterConfig9Interface, dshow.ivmrfilterconfig9, vmr9/IVMRFilterConfig9
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRFilterConfig9
 - vmr9/IVMRFilterConfig9
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
 - IVMRFilterConfig9
---

# IVMRFilterConfig9 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRFilterConfig9</code> interface is implemented by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>. Applications use this interface to configure the VMR's operating mode and video rendering mechanisms. Applications must add the VMR to the graph and configure it before it is connected to any upstream filters (for example, in a call to <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>). Once a filter has been connected to the VMR, the VMR's configuration is locked and all future attempts to alter it fail.

## -inheritance

The <b>IVMRFilterConfig9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRFilterConfig9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
