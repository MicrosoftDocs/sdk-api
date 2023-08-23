---
UID: NF:strmif.IVMRSurfaceAllocator.PrepareSurface
title: IVMRSurfaceAllocator::PrepareSurface (strmif.h)
description: The PrepareSurface method prepares the DirectDraw surface to have the next video frame decoded into it.
helpviewer_keywords: ["IVMRSurfaceAllocator interface [DirectShow]","PrepareSurface method","IVMRSurfaceAllocator.PrepareSurface","IVMRSurfaceAllocator::PrepareSurface","IVMRSurfaceAllocatorPrepareSurface","PrepareSurface","PrepareSurface method [DirectShow]","PrepareSurface method [DirectShow]","IVMRSurfaceAllocator interface","dshow.ivmrsurfaceallocator_preparesurface","strmif/IVMRSurfaceAllocator::PrepareSurface"]
old-location: dshow\ivmrsurfaceallocator_preparesurface.htm
tech.root: dshow
ms.assetid: 5978bd6e-1aee-4e5e-9d28-f60e20b5b3e7
ms.date: 4/26/2023
ms.keywords: IVMRSurfaceAllocator interface [DirectShow],PrepareSurface method, IVMRSurfaceAllocator.PrepareSurface, IVMRSurfaceAllocator::PrepareSurface, IVMRSurfaceAllocatorPrepareSurface, PrepareSurface, PrepareSurface method [DirectShow], PrepareSurface method [DirectShow],IVMRSurfaceAllocator interface, dshow.ivmrsurfaceallocator_preparesurface, strmif/IVMRSurfaceAllocator::PrepareSurface
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
 - IVMRSurfaceAllocator::PrepareSurface
 - strmif/IVMRSurfaceAllocator::PrepareSurface
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
 - IVMRSurfaceAllocator.PrepareSurface
---

# IVMRSurfaceAllocator::PrepareSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>PrepareSurface</code> method prepares the DirectDraw surface to have the next video frame decoded into it.

## -parameters

### -param dwUserID [in]

An application-defined DWORD_PTR cookie that uniquely identifies this instance of the VMR for use in scenarios when one instance of the allocator-presenter is used with multiple VMR instances.

### -param lpSurface [in]

Specifies the DirectDraw surface

### -param dwSurfaceFlags [in]

Double word containing the surface flags. See Remarks.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The only flag that the VMR currently checks here is AM_GBF_NOTASYNCPOINT (0x00000002), which indicates that you are not going to fill this buffer with a sync point (keyframe).

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocator">IVMRSurfaceAllocator Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>