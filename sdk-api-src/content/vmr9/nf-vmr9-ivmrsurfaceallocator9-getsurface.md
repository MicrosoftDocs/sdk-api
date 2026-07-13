---
UID: NF:vmr9.IVMRSurfaceAllocator9.GetSurface
title: IVMRSurfaceAllocator9::GetSurface (vmr9.h)
description: The GetSurface method gets a Direct3D surface from the allocator-presenter.
helpviewer_keywords: ["GetSurface","GetSurface method [DirectShow]","GetSurface method [DirectShow]","IVMRSurfaceAllocator9 interface","IVMRSurfaceAllocator9 interface [DirectShow]","GetSurface method","IVMRSurfaceAllocator9.GetSurface","IVMRSurfaceAllocator9::GetSurface","IVMRSurfaceAllocator9GetSurface","dshow.ivmrsurfaceallocator9_getsurface","vmr9/IVMRSurfaceAllocator9::GetSurface"]
old-location: dshow\ivmrsurfaceallocator9_getsurface.htm
tech.root: dshow
ms.assetid: b14c7744-b5e5-484e-b5f3-99c4185a4e7c
ms.date: 4/26/2023
ms.keywords: GetSurface, GetSurface method [DirectShow], GetSurface method [DirectShow],IVMRSurfaceAllocator9 interface, IVMRSurfaceAllocator9 interface [DirectShow],GetSurface method, IVMRSurfaceAllocator9.GetSurface, IVMRSurfaceAllocator9::GetSurface, IVMRSurfaceAllocator9GetSurface, dshow.ivmrsurfaceallocator9_getsurface, vmr9/IVMRSurfaceAllocator9::GetSurface
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
 - IVMRSurfaceAllocator9::GetSurface
 - vmr9/IVMRSurfaceAllocator9::GetSurface
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
 - IVMRSurfaceAllocator9.GetSurface
---

# IVMRSurfaceAllocator9::GetSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetSurface</b> method gets a Direct3D surface from the allocator-presenter.

## -parameters

### -param dwUserID [in]

Application-defined identifier. This value is the same value that the application passed to the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator">IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator</a> method in the <i>dwUserID</i> parameter.

### -param SurfaceIndex [in]

Specifies the index of the surface to retrieve.

### -param SurfaceFlags [in]

Reserved.

### -param lplpSurface [out]

Receives a pointer to the <b>IDirect3DSurface9</b> interface. The caller must release the interface.

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



<a href="/windows/desktop/DirectShow/supplying-a-custom-allocator-presenter-for-vmr-9">Supplying a Custom Allocator-Presenter for VMR-9</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>