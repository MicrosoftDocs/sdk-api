---
UID: NF:strmif.IVMRSurfaceAllocatorNotify.NotifyEvent
title: IVMRSurfaceAllocatorNotify::NotifyEvent (strmif.h)
description: The NotifyEvent method is called by the allocator-presenter to inform the VMR of any significant DirectShow events during the allocation or presentation processes.
helpviewer_keywords: ["IVMRSurfaceAllocatorNotify interface [DirectShow]","NotifyEvent method","IVMRSurfaceAllocatorNotify.NotifyEvent","IVMRSurfaceAllocatorNotify::NotifyEvent","IVMRSurfaceAllocatorNotifyNotifyEvent","NotifyEvent","NotifyEvent method [DirectShow]","NotifyEvent method [DirectShow]","IVMRSurfaceAllocatorNotify interface","dshow.ivmrsurfaceallocatornotify_notifyevent","strmif/IVMRSurfaceAllocatorNotify::NotifyEvent"]
old-location: dshow\ivmrsurfaceallocatornotify_notifyevent.htm
tech.root: dshow
ms.assetid: 566a889b-e6dc-42e7-ba71-0b0a17f3ae8c
ms.date: 4/26/2023
ms.keywords: IVMRSurfaceAllocatorNotify interface [DirectShow],NotifyEvent method, IVMRSurfaceAllocatorNotify.NotifyEvent, IVMRSurfaceAllocatorNotify::NotifyEvent, IVMRSurfaceAllocatorNotifyNotifyEvent, NotifyEvent, NotifyEvent method [DirectShow], NotifyEvent method [DirectShow],IVMRSurfaceAllocatorNotify interface, dshow.ivmrsurfaceallocatornotify_notifyevent, strmif/IVMRSurfaceAllocatorNotify::NotifyEvent
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
 - IVMRSurfaceAllocatorNotify::NotifyEvent
 - strmif/IVMRSurfaceAllocatorNotify::NotifyEvent
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
 - IVMRSurfaceAllocatorNotify.NotifyEvent
---

# IVMRSurfaceAllocatorNotify::NotifyEvent


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>NotifyEvent</code> method is called by the allocator-presenter to inform the VMR of any significant DirectShow events during the allocation or presentation processes.

## -parameters

### -param EventCode [in]

Specifies the event code.

### -param Param1 [in]

Specifies Param1 of the event code.

### -param Param2 [in]

Specifies Param2 of the event code.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The VMR provides the allocator-presenter with a pointer to this interface in a call to <a href="/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocator-advisenotify">IVMRSurfaceAllocator::AdviseNotify</a>. When the allocator-presenter calls this method and specifies some regular DirectShow event, such as EC_ERRORABORT or EC_VMR_RENDERDEVICE_SET, the VMR will pass the event to the filter graph manager.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocatornotify">IVMRSurfaceAllocatorNotify Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>