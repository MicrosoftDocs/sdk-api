---
UID: NN:vmr9.IVMRSurface9
title: IVMRSurface9 (vmr9.h)
description: The IVMRSurface9 interface is implemented on the media samples used by the Video Mixing Renderer Filter 9.
old-location: dshow\ivmrsurface9.htm
tech.root: DirectShow
ms.assetid: b24dae7d-5e88-4973-8507-8bd13cdccbde
ms.date: 12/05/2018
ms.keywords: IVMRSurface9, IVMRSurface9 interface [DirectShow], IVMRSurface9 interface [DirectShow],described, IVMRSurface9Interface, dshow.ivmrsurface9, vmr9/IVMRSurface9
f1_keywords:
- vmr9/IVMRSurface9
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
- IVMRSurface9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurface9 interface


## -description



The <code>IVMRSurface9</code> interface is implemented on the media samples used by the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>. Filters can use this interface to access the underlying Direct3D surface on which the media sample is based. Filters must always lock and unlock the surface using the methods available on this interface. Filters must never call lock or unlock directly on the Direct3D surface interface returned from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurface-getsurface">GetSurface</a> method. Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurface9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurface9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRSurface9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurface9-getsurface">GetSurface</a>
</td>
<td align="left" width="63%">
Retrieves the attached Direct3D surface interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurface9-issurfacelocked">IsSurfaceLocked</a>
</td>
<td align="left" width="63%">
Indicates whether the Direct3D surface attached to this media sample is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurface9-locksurface">LockSurface</a>
</td>
<td align="left" width="63%">
Locks the attached Direct3D surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurface9-unlocksurface">UnlockSurface</a>
</td>
<td align="left" width="63%">
Unlocks the attached Direct3D surface.

</td>
</tr>
</table> 


## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

