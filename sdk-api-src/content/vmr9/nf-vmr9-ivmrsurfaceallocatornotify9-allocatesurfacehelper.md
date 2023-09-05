---
UID: NF:vmr9.IVMRSurfaceAllocatorNotify9.AllocateSurfaceHelper
title: IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper (vmr9.h)
description: The AllocateSurfaceHelper method allocates a Direct3D surface based on application-specified parameters.
helpviewer_keywords: ["AllocateSurfaceHelper","AllocateSurfaceHelper method [DirectShow]","AllocateSurfaceHelper method [DirectShow]","IVMRSurfaceAllocatorNotify9 interface","IVMRSurfaceAllocatorNotify9 interface [DirectShow]","AllocateSurfaceHelper method","IVMRSurfaceAllocatorNotify9.AllocateSurfaceHelper","IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper","IVMRSurfaceAllocatorNotify9AllocateSurfaceHelper","dshow.ivmrsurfaceallocatornotify9_allocatesurfacehelper","vmr9/IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper"]
old-location: dshow\ivmrsurfaceallocatornotify9_allocatesurfacehelper.htm
tech.root: dshow
ms.assetid: b69db9e9-6ab0-40ad-b929-30613c0b9e4b
ms.date: 4/26/2023
ms.keywords: AllocateSurfaceHelper, AllocateSurfaceHelper method [DirectShow], AllocateSurfaceHelper method [DirectShow],IVMRSurfaceAllocatorNotify9 interface, IVMRSurfaceAllocatorNotify9 interface [DirectShow],AllocateSurfaceHelper method, IVMRSurfaceAllocatorNotify9.AllocateSurfaceHelper, IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper, IVMRSurfaceAllocatorNotify9AllocateSurfaceHelper, dshow.ivmrsurfaceallocatornotify9_allocatesurfacehelper, vmr9/IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper
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
 - IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper
 - vmr9/IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper
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
 - IVMRSurfaceAllocatorNotify9.AllocateSurfaceHelper
---

# IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AllocateSurfaceHelper</code> method allocates a Direct3D surface based on application-specified parameters.



If you are implementing a custom allocator-presenter for the VMR-9, you can use this method to allocate the surfaces.

## -parameters

### -param lpAllocInfo [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9allocationinfo">VMR9AllocationInfo</a> structure that describes the surfaces to create.

### -param lpNumBuffers [in, out]

On input, this parameter specifies the number of surfaces to create. On output, this parameter contains the number of surfaces that the method created.

### -param lplpSurface [out]

Address of an array of <b>IDirect3DSurface9</b> interface pointers. The size of the array must equal the value in <i>lpNumBuffers</i>. The method fills the array with valid <b>IDirect3DSurface9</b> pointers for each Direct3D surface that it creates. The caller must release the interface pointers. (Do not put any valid pointers into the array before you call this method, because the method will overwrite them, causing a memory leak.)

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

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatornotify9">IVMRSurfaceAllocatorNotify9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>