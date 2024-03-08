---
UID: NN:strmif.IVMRSurface
title: IVMRSurface (strmif.h)
description: The IVMRSurface interface is implemented on the media samples used by the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRSurface","IVMRSurface interface [DirectShow]","IVMRSurface interface [DirectShow]","described","IVMRSurfaceInterface","dshow.ivmrsurface","strmif/IVMRSurface"]
old-location: dshow\ivmrsurface.htm
tech.root: dshow
ms.assetid: 8222ea5c-be77-4f33-83ff-073fb3e85e73
ms.date: 4/26/2023
ms.keywords: IVMRSurface, IVMRSurface interface [DirectShow], IVMRSurface interface [DirectShow],described, IVMRSurfaceInterface, dshow.ivmrsurface, strmif/IVMRSurface
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
 - IVMRSurface
 - strmif/IVMRSurface
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
 - IVMRSurface
---

# IVMRSurface interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRSurface</code> interface is implemented on the media samples used by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). Filters can use this interface to access the underlying DirectDraw surface on which the media sample is based. Filters must always lock and unlock the surface using the methods available on this interface. Filters must never call lock or unlock directly on the DirectDraw surface interface returned from the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrsurface-getsurface">GetSurface</a> method. Applications do not use this interface.

## -inheritance

The <b>IVMRSurface</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurface</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
