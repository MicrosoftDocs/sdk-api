---
UID: NF:strmif.IVMRSurfaceAllocatorNotify.AdviseSurfaceAllocator
title: IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator (strmif.h)
description: The AdviseSurfaceAllocator method is called by an application to instruct the VMR to use a custom allocator-presenter.
helpviewer_keywords: ["AdviseSurfaceAllocator","AdviseSurfaceAllocator method [DirectShow]","AdviseSurfaceAllocator method [DirectShow]","IVMRSurfaceAllocatorNotify interface","IVMRSurfaceAllocatorNotify interface [DirectShow]","AdviseSurfaceAllocator method","IVMRSurfaceAllocatorNotify.AdviseSurfaceAllocator","IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator","IVMRSurfaceAllocatorNotifyAdviseSurfaceAllocator","dshow.ivmrsurfaceallocatornotify_advisesurfaceallocator","strmif/IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator"]
old-location: dshow\ivmrsurfaceallocatornotify_advisesurfaceallocator.htm
tech.root: dshow
ms.assetid: fdb0837c-1ee3-4dc9-b797-3d726c8ba3dc
ms.date: 4/26/2023
ms.keywords: AdviseSurfaceAllocator, AdviseSurfaceAllocator method [DirectShow], AdviseSurfaceAllocator method [DirectShow],IVMRSurfaceAllocatorNotify interface, IVMRSurfaceAllocatorNotify interface [DirectShow],AdviseSurfaceAllocator method, IVMRSurfaceAllocatorNotify.AdviseSurfaceAllocator, IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator, IVMRSurfaceAllocatorNotifyAdviseSurfaceAllocator, dshow.ivmrsurfaceallocatornotify_advisesurfaceallocator, strmif/IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator
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
 - IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator
 - strmif/IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator
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
 - IVMRSurfaceAllocatorNotify.AdviseSurfaceAllocator
---

# IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AdviseSurfaceAllocator</code> method is called by an application to instruct the VMR to use a custom allocator-presenter.

## -parameters

### -param dwUserID [in]

An application-defined DWORD_PTR that uniquely identifies this instance of the VMR in scenarios when multiple instances of the VMR are being used with a single instance of an allocator-presenter.

### -param lpIVRMSurfaceAllocator [in]

Specifies the <a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocator">IVMRSurfaceAllocator</a> interface on the new allocator-presenter. If this value is <b>NULL</b>, then the VMR will release the client allocator-presenter and restore its default allocator-presenter.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The method will cause the default allocator-presenter to be uninstalled and destroyed, and replaced with the specified new component. The new component must also support the <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenter">IVMRImagePresenter</a> interface.

This method can be called only once in the lifetime of the VMR. The VMR continues to use the allocator-presenter until the VMR is itself deleted. When the VMR is finally released, it releases its reference count on the custom allocator-presenter object, which allows that object to be freed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocatornotify">IVMRSurfaceAllocatorNotify Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>