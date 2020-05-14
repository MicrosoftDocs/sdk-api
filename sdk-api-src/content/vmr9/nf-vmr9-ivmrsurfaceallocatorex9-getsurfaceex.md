---
UID: NF:vmr9.IVMRSurfaceAllocatorEx9.GetSurfaceEx
title: IVMRSurfaceAllocatorEx9::GetSurfaceEx (vmr9.h)
description: The GetSurfaceEx method retrieves a Direct3D surface and a destination rectangle.helpviewer_keywords: ["GetSurfaceEx","GetSurfaceEx method [DirectShow]","GetSurfaceEx method [DirectShow]","IVMRSurfaceAllocatorEx9 interface","IVMRSurfaceAllocatorEx9 interface [DirectShow]","GetSurfaceEx method","IVMRSurfaceAllocatorEx9.GetSurfaceEx","IVMRSurfaceAllocatorEx9::GetSurfaceEx","IVMRSurfaceAllocatorEx9GetSurfaceEx","dshow.ivmrsurfaceallocatorex9_getsurfaceex","vmr9/IVMRSurfaceAllocatorEx9::GetSurfaceEx"]
old-location: dshow\ivmrsurfaceallocatorex9_getsurfaceex.htm
tech.root: DirectShow
ms.assetid: 828f1ea6-4093-4a33-bc41-0f6fff752bcf
ms.date: 12/05/2018
ms.keywords: GetSurfaceEx, GetSurfaceEx method [DirectShow], GetSurfaceEx method [DirectShow],IVMRSurfaceAllocatorEx9 interface, IVMRSurfaceAllocatorEx9 interface [DirectShow],GetSurfaceEx method, IVMRSurfaceAllocatorEx9.GetSurfaceEx, IVMRSurfaceAllocatorEx9::GetSurfaceEx, IVMRSurfaceAllocatorEx9GetSurfaceEx, dshow.ivmrsurfaceallocatorex9_getsurfaceex, vmr9/IVMRSurfaceAllocatorEx9::GetSurfaceEx
f1_keywords:
- vmr9/IVMRSurfaceAllocatorEx9.GetSurfaceEx
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVMRSurfaceAllocatorEx9.GetSurfaceEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurfaceAllocatorEx9::GetSurfaceEx


## -description


The <b>GetSurfaceEx</b> method retrieves a Direct3D surface and a destination rectangle.


## -parameters




### -param dwUserID [in]

Application-defined identifier. This value is the same value that the application passed to the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator">IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator</a> method in the <i>dwUserID</i> parameter..


### -param SurfaceIndex [in]

Index of the surface to retrieve.


### -param SurfaceFlags [in]

Surface flags.


### -param lplpSurface [out]

Receives a pointer to the <b>IDirect3DSurface9</b> interface. The caller must release the interface.


### -param lprcDst [out]

Location within the surface where the VMR-9 should write the composited image.


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




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatorex9">IVMRSurfaceAllocatorEx9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

