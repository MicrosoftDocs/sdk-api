---
UID: NN:vmr9.IVMRSurfaceAllocatorEx9
title: IVMRSurfaceAllocatorEx9 (vmr9.h)
description: The IVMRSurfaceAllocatorEx9 interface provides a way for custom allocator-presenters to control where the Video Mixing Renderer Filter 9 (VMR-9) draws the composited image.
helpviewer_keywords: ["IVMRSurfaceAllocatorEx9","IVMRSurfaceAllocatorEx9 interface [DirectShow]","IVMRSurfaceAllocatorEx9 interface [DirectShow]","described","IVMRSurfaceAllocatorEx9Interface","dshow.ivmrsurfaceallocatorex9","vmr9/IVMRSurfaceAllocatorEx9"]
old-location: dshow\ivmrsurfaceallocatorex9.htm
tech.root: dshow
ms.assetid: 4c43867f-6c4b-4ed7-af83-0133c997efcb
ms.date: 4/26/2023
ms.keywords: IVMRSurfaceAllocatorEx9, IVMRSurfaceAllocatorEx9 interface [DirectShow], IVMRSurfaceAllocatorEx9 interface [DirectShow],described, IVMRSurfaceAllocatorEx9Interface, dshow.ivmrsurfaceallocatorex9, vmr9/IVMRSurfaceAllocatorEx9
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
 - IVMRSurfaceAllocatorEx9
 - vmr9/IVMRSurfaceAllocatorEx9
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
 - IVMRSurfaceAllocatorEx9
---

# IVMRSurfaceAllocatorEx9 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IVMRSurfaceAllocatorEx9</b> interface provides a way for custom allocator-presenters to control where the Video Mixing Renderer Filter 9 (VMR-9) draws the composited image.



To use this interface, implement it on your allocator-presenter. At the start of each frame, the VMR-9 calls <b>QueryInterface</b> on the allocator-presenter for the <b>IVMRSurfaceAllocatorEx9</b> interface. If the allocator-presenter returns the interface, the VMR-9 calls the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocatorex9-getsurfaceex">IVMRSurfaceAllocatorEx9::GetSurfaceEx</a> method instead of the usual <a href="/windows/desktop/api/strmif/nf-strmif-ivmrsurface-getsurface">IVMRSurfaceAllocator9::GetSurface</a> method. This enables your allocator-presenter to specify the rectangle within the returned <b>IDirect3DSurface9</b> where the composed video image will be written. This feature enables all of the video image scaling operations to be performed in a single stage, and is available in both RGB and YUV mixing modes.

## -inheritance

The <b>IVMRSurfaceAllocatorEx9</b> interface inherits from <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9">IVMRSurfaceAllocator9</a>. <b>IVMRSurfaceAllocatorEx9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9">IVMRSurfaceAllocator9</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
