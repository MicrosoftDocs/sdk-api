---
UID: NN:vmr9.IVMRSurface9
title: IVMRSurface9 (vmr9.h)
author: windows-sdk-content
description: The IVMRSurface9 interface is implemented on the media samples used by the Video Mixing Renderer Filter 9.
old-location: dshow\ivmrsurface9.htm
tech.root: DirectShow
ms.assetid: b24dae7d-5e88-4973-8507-8bd13cdccbde
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRSurface9, IVMRSurface9 interface [DirectShow], IVMRSurface9 interface [DirectShow],described, IVMRSurface9Interface, dshow.ivmrsurface9, vmr9/IVMRSurface9
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRSurface9 interface


## -description



The <code>IVMRSurface9</code> interface is implemented on the media samples used by the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a>. Filters can use this interface to access the underlying Direct3D surface on which the media sample is based. Filters must always lock and unlock the surface using the methods available on this interface. Filters must never call lock or unlock directly on the Direct3D surface interface returned from the <a href="https://msdn.microsoft.com/en-us/library/Dd390524(v=VS.85).aspx">GetSurface</a> method. Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurface9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRSurface9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd390495(v=VS.85).aspx">GetSurface</a>
</td>
<td align="left" width="63%">
Retrieves the attached Direct3D surface interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390496(v=VS.85).aspx">IsSurfaceLocked</a>
</td>
<td align="left" width="63%">
Indicates whether the Direct3D surface attached to this media sample is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390497(v=VS.85).aspx">LockSurface</a>
</td>
<td align="left" width="63%">
Locks the attached Direct3D surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390498(v=VS.85).aspx">UnlockSurface</a>
</td>
<td align="left" width="63%">
Unlocks the attached Direct3D surface.

</td>
</tr>
</table> 


## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

