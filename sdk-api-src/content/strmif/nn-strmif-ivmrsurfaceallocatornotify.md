---
UID: NN:strmif.IVMRSurfaceAllocatorNotify
title: IVMRSurfaceAllocatorNotify (strmif.h)
description: The IVMRSurfaceAllocatorNotify interface is implemented by the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRSurfaceAllocatorNotify","IVMRSurfaceAllocatorNotify interface [DirectShow]","IVMRSurfaceAllocatorNotify interface [DirectShow]","described","IVMRSurfaceAllocatorNotifyInterface","dshow.ivmrsurfaceallocatornotify","strmif/IVMRSurfaceAllocatorNotify"]
old-location: dshow\ivmrsurfaceallocatornotify.htm
tech.root: dshow
ms.assetid: c590c4cb-43ba-41c2-ab1f-28f7aeee0c87
ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocatorNotify, IVMRSurfaceAllocatorNotify interface [DirectShow], IVMRSurfaceAllocatorNotify interface [DirectShow],described, IVMRSurfaceAllocatorNotifyInterface, dshow.ivmrsurfaceallocatornotify, strmif/IVMRSurfaceAllocatorNotify
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
 - IVMRSurfaceAllocatorNotify
 - strmif/IVMRSurfaceAllocatorNotify
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
 - IVMRSurfaceAllocatorNotify
---

# IVMRSurfaceAllocatorNotify interface


## -description

The <code>IVMRSurfaceAllocatorNotify</code> interface is implemented by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). Applications use this interface to set a custom allocator-presenter and the allocator-presenter uses this interface to inform the VMR-7 of changes to the system environment that affect the DirectDraw surfaces.

In order for an application to obtain this interface, the VMR must be in renderless mode.

For the VMR-9, use the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatornotify9">IVMRSurfaceAllocatorNotify9</a> interface.

## -inheritance

The <b>IVMRSurfaceAllocatorNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurfaceAllocatorNotify</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
