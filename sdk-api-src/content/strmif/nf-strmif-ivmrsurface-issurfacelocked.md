---
UID: NF:strmif.IVMRSurface.IsSurfaceLocked
title: IVMRSurface::IsSurfaceLocked (strmif.h)
description: The IsSurfaceLocked method indicates whether the DirectDraw surface attached to this media sample is locked.
helpviewer_keywords: ["IVMRSurface interface [DirectShow]","IsSurfaceLocked method","IVMRSurface.IsSurfaceLocked","IVMRSurface::IsSurfaceLocked","IVMRSurfaceIsSurfaceLocked","IsSurfaceLocked","IsSurfaceLocked method [DirectShow]","IsSurfaceLocked method [DirectShow]","IVMRSurface interface","dshow.ivmrsurface_issurfacelocked","strmif/IVMRSurface::IsSurfaceLocked"]
old-location: dshow\ivmrsurface_issurfacelocked.htm
tech.root: dshow
ms.assetid: 690194c2-2f40-414f-9130-f2f9c44fe71e
ms.date: 4/26/2023
ms.keywords: IVMRSurface interface [DirectShow],IsSurfaceLocked method, IVMRSurface.IsSurfaceLocked, IVMRSurface::IsSurfaceLocked, IVMRSurfaceIsSurfaceLocked, IsSurfaceLocked, IsSurfaceLocked method [DirectShow], IsSurfaceLocked method [DirectShow],IVMRSurface interface, dshow.ivmrsurface_issurfacelocked, strmif/IVMRSurface::IsSurfaceLocked
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
 - IVMRSurface::IsSurfaceLocked
 - strmif/IVMRSurface::IsSurfaceLocked
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
 - IVMRSurface.IsSurfaceLocked
---

# IVMRSurface::IsSurfaceLocked


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsSurfaceLocked</code> method indicates whether the DirectDraw surface attached to this media sample is locked.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurface">IVMRSurface Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
