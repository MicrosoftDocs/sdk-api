---
UID: NF:strmif.IVMRSurfaceAllocator.AdviseNotify
title: IVMRSurfaceAllocator::AdviseNotify (strmif.h)
description: The AdviseNotify method provides the allocator-presenter with the VMR-7 filter's interface for notification callbacks.
helpviewer_keywords: ["AdviseNotify","AdviseNotify method [DirectShow]","AdviseNotify method [DirectShow]","IVMRSurfaceAllocator interface","IVMRSurfaceAllocator interface [DirectShow]","AdviseNotify method","IVMRSurfaceAllocator.AdviseNotify","IVMRSurfaceAllocator::AdviseNotify","IVMRSurfaceAllocatorAdviseNotify","dshow.ivmrsurfaceallocator_advisenotify","strmif/IVMRSurfaceAllocator::AdviseNotify"]
old-location: dshow\ivmrsurfaceallocator_advisenotify.htm
tech.root: dshow
ms.assetid: d4d9998f-e7d6-4c06-8a37-2e9c8e29106b
ms.date: 4/26/2023
ms.keywords: AdviseNotify, AdviseNotify method [DirectShow], AdviseNotify method [DirectShow],IVMRSurfaceAllocator interface, IVMRSurfaceAllocator interface [DirectShow],AdviseNotify method, IVMRSurfaceAllocator.AdviseNotify, IVMRSurfaceAllocator::AdviseNotify, IVMRSurfaceAllocatorAdviseNotify, dshow.ivmrsurfaceallocator_advisenotify, strmif/IVMRSurfaceAllocator::AdviseNotify
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
 - IVMRSurfaceAllocator::AdviseNotify
 - strmif/IVMRSurfaceAllocator::AdviseNotify
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
 - IVMRSurfaceAllocator.AdviseNotify
---

# IVMRSurfaceAllocator::AdviseNotify


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AdviseNotify</code> method provides the allocator-presenter with the VMR-7 filter's interface for notification callbacks. If you are using a custom allocator-presenter, the application must call this method on the allocator-presenter, with a pointer to the VMR's <b>IVMRSurfaceAllocatorNotify</b> interface. The allocator-presenter uses this interface to communicate with the VMR.



If you are not using a custom allocator-presenter, the application does not have to call this method.

## -parameters

### -param lpIVMRSurfAllocNotify [in]

Specifies the <a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocatornotify">IVMRSurfaceAllocatorNotify</a> interface pointer that the allocator-presenter will use to pass notifications back to the VMR.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocator">IVMRSurfaceAllocator Interface</a>



<a href="/windows/desktop/DirectShow/supplying-a-custom-allocator-presenter-for-vmr-7">Supplying a Custom Allocator-Presenter for VMR-7</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/vmr-renderless-playback-mode--custom-allocator-presenters">VMR Renderless Playback Mode (Custom Allocator-Presenters)</a>