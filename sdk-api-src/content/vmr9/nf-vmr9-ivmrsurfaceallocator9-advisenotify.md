---
UID: NF:vmr9.IVMRSurfaceAllocator9.AdviseNotify
title: IVMRSurfaceAllocator9::AdviseNotify (vmr9.h)
description: The AdviseNotify method provides the allocator-presenter with the VMR-9 filter's interface for notification callbacks.
helpviewer_keywords: ["AdviseNotify","AdviseNotify method [DirectShow]","AdviseNotify method [DirectShow]","IVMRSurfaceAllocator9 interface","IVMRSurfaceAllocator9 interface [DirectShow]","AdviseNotify method","IVMRSurfaceAllocator9.AdviseNotify","IVMRSurfaceAllocator9::AdviseNotify","IVMRSurfaceAllocator9AdviseNotify","dshow.ivmrsurfaceallocator9_advisenotify","vmr9/IVMRSurfaceAllocator9::AdviseNotify"]
old-location: dshow\ivmrsurfaceallocator9_advisenotify.htm
tech.root: dshow
ms.assetid: 2c367444-50bf-4fbe-b2d9-ed32275576e9
ms.date: 4/26/2023
ms.keywords: AdviseNotify, AdviseNotify method [DirectShow], AdviseNotify method [DirectShow],IVMRSurfaceAllocator9 interface, IVMRSurfaceAllocator9 interface [DirectShow],AdviseNotify method, IVMRSurfaceAllocator9.AdviseNotify, IVMRSurfaceAllocator9::AdviseNotify, IVMRSurfaceAllocator9AdviseNotify, dshow.ivmrsurfaceallocator9_advisenotify, vmr9/IVMRSurfaceAllocator9::AdviseNotify
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
 - IVMRSurfaceAllocator9::AdviseNotify
 - vmr9/IVMRSurfaceAllocator9::AdviseNotify
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
 - IVMRSurfaceAllocator9.AdviseNotify
---

# IVMRSurfaceAllocator9::AdviseNotify


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AdviseNotify</b> method provides the allocator-presenter with the VMR-9 filter's interface for notification callbacks. If you are using a custom allocator-presenter, the application must call this method on the allocator-presenter, with a pointer to the VMR's <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatornotify9">IVMRSurfaceAllocatorNotify9</a> interface. The allocator-presenter uses this interface to communicate with the VMR.



If you are not using a custom allocator-presenter, the application does not have to call this method.

## -parameters

### -param lpIVMRSurfAllocNotify [in]

Specifies the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatornotify9">IVMRSurfaceAllocatorNotify9</a> interface that the allocator-presenter will use to pass notifications back to the VMR.

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

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9">IVMRSurfaceAllocator9 Interface</a>



<a href="/windows/desktop/DirectShow/supplying-a-custom-allocator-presenter-for-vmr-7">Supplying a Custom Allocator-Presenter for VMR-7</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/vmr-renderless-playback-mode--custom-allocator-presenters">VMR Renderless Playback Mode (Custom Allocator-Presenters)</a>