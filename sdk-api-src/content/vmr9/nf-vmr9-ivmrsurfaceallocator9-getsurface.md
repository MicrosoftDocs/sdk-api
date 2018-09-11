---
UID: NF:vmr9.IVMRSurfaceAllocator9.GetSurface
title: IVMRSurfaceAllocator9::GetSurface
author: windows-sdk-content
description: The GetSurface method gets a Direct3D surface from the allocator-presenter.
old-location: dshow\ivmrsurfaceallocator9_getsurface.htm
tech.root: DirectShow
ms.assetid: b14c7744-b5e5-484e-b5f3-99c4185a4e7c
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetSurface, GetSurface method [DirectShow], GetSurface method [DirectShow],IVMRSurfaceAllocator9 interface, IVMRSurfaceAllocator9 interface [DirectShow],GetSurface method, IVMRSurfaceAllocator9.GetSurface, IVMRSurfaceAllocator9::GetSurface, IVMRSurfaceAllocator9GetSurface, dshow.ivmrsurfaceallocator9_getsurface, vmr9/IVMRSurfaceAllocator9::GetSurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IVMRSurfaceAllocator9.GetSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRSurfaceAllocator9::GetSurface


## -description



The <b>GetSurface</b> method gets a Direct3D surface from the allocator-presenter.




## -parameters




### -param dwUserID [in]

Application-defined identifier. This value is the same value that the application passed to the <a href="https://msdn.microsoft.com/99f9c549-e4b1-480b-97a4-7a29c9cdb649">IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator</a> method in the <i>dwUserID</i> parameter.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/dd187168-19c7-414c-a764-f180d1d310f2">IVMRSurfaceAllocator9 Interface</a>



<a href="https://msdn.microsoft.com/61bb6b0d-25b5-481b-a241-74c6e421f109">Supplying a Custom Allocator-Presenter for VMR-9</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

