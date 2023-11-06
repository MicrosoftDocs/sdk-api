---
UID: NF:vmr9.IVMRSurfaceAllocatorNotify9.AdviseSurfaceAllocator
title: IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator (vmr9.h)
description: The AdviseSurfaceAllocator method is called by an application to instruct the VMR-9 to use a custom allocator-presenter.
helpviewer_keywords: ["AdviseSurfaceAllocator","AdviseSurfaceAllocator method [DirectShow]","AdviseSurfaceAllocator method [DirectShow]","IVMRSurfaceAllocatorNotify9 interface","IVMRSurfaceAllocatorNotify9 interface [DirectShow]","AdviseSurfaceAllocator method","IVMRSurfaceAllocatorNotify9.AdviseSurfaceAllocator","IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator","IVMRSurfaceAllocatorNotify9AdviseSurfaceAllocator","dshow.ivmrsurfaceallocatornotify9_advisesurfaceallocator","vmr9/IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator"]
old-location: dshow\ivmrsurfaceallocatornotify9_advisesurfaceallocator.htm
tech.root: dshow
ms.assetid: 99f9c549-e4b1-480b-97a4-7a29c9cdb649
ms.date: 4/26/2023
ms.keywords: AdviseSurfaceAllocator, AdviseSurfaceAllocator method [DirectShow], AdviseSurfaceAllocator method [DirectShow],IVMRSurfaceAllocatorNotify9 interface, IVMRSurfaceAllocatorNotify9 interface [DirectShow],AdviseSurfaceAllocator method, IVMRSurfaceAllocatorNotify9.AdviseSurfaceAllocator, IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator, IVMRSurfaceAllocatorNotify9AdviseSurfaceAllocator, dshow.ivmrsurfaceallocatornotify9_advisesurfaceallocator, vmr9/IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator
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
 - IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator
 - vmr9/IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator
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
 - IVMRSurfaceAllocatorNotify9.AdviseSurfaceAllocator
---

# IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AdviseSurfaceAllocator</code> method is called by an application to instruct the VMR-9 to use a custom allocator-presenter.

## -parameters

### -param dwUserID [in]

Application-defined value that identifies this instance of the VMR-9.

### -param lpIVRMSurfaceAllocator [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9">IVMRSurfaceAllocator9</a> interface on the custom surface allocator object.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method can be called only once in the lifetime of the VMR. The VMR continues to use the allocator-presenter until the VMR is itself deleted. When the VMR is finally released, it releases its reference count on the custom allocator-presenter object, which allows that object to be freed.

The custom allocator-presenter must also support the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenter9">IVMRImagePresenter9</a> interface.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatornotify9">IVMRSurfaceAllocatorNotify9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>