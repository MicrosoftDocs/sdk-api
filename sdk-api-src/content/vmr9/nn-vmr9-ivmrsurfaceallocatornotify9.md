---
UID: NN:vmr9.IVMRSurfaceAllocatorNotify9
title: IVMRSurfaceAllocatorNotify9 (vmr9.h)
description: The IVMRSurfaceAllocatorNotify9 interface is implemented by the Video Mixing Renderer Filter 9 (VMR-9).
helpviewer_keywords: ["IVMRSurfaceAllocatorNotify9","IVMRSurfaceAllocatorNotify9 interface [DirectShow]","IVMRSurfaceAllocatorNotify9 interface [DirectShow]","described","IVMRSurfaceAllocatorNotify9Interface","dshow.ivmrsurfaceallocatornotify9","vmr9/IVMRSurfaceAllocatorNotify9"]
old-location: dshow\ivmrsurfaceallocatornotify9.htm
tech.root: dshow
ms.assetid: f275b835-e5b3-46f4-8b26-a4b0e2554c7c
ms.date: 4/26/2023
ms.keywords: IVMRSurfaceAllocatorNotify9, IVMRSurfaceAllocatorNotify9 interface [DirectShow], IVMRSurfaceAllocatorNotify9 interface [DirectShow],described, IVMRSurfaceAllocatorNotify9Interface, dshow.ivmrsurfaceallocatornotify9, vmr9/IVMRSurfaceAllocatorNotify9
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
 - IVMRSurfaceAllocatorNotify9
 - vmr9/IVMRSurfaceAllocatorNotify9
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
 - IVMRSurfaceAllocatorNotify9
---

# IVMRSurfaceAllocatorNotify9 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IVMRSurfaceAllocatorNotify9</b> interface is implemented by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). Applications use this interface to set a custom allocator-presenter and the allocator-presenter uses this interface to inform the VMR of changes to the system environment that affect the Direct3D surfaces.

## -inheritance

The <b>IVMRSurfaceAllocatorNotify9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurfaceAllocatorNotify9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

The VMR-9 supports this interface in renderless mode only. Otherwise, <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> returns <b>E_NOINTERFACE</b>. For more information, see <a href="/windows/desktop/DirectShow/vmr-modes-of-operation">VMR Modes of Operation</a>.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>
