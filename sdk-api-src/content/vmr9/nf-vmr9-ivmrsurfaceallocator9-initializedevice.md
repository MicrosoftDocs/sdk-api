---
UID: NF:vmr9.IVMRSurfaceAllocator9.InitializeDevice
title: IVMRSurfaceAllocator9::InitializeDevice
author: windows-sdk-content
description: The InitializeDevice method is called by the Video Mixing Renderer 9 (VMR-9) when it needs the allocator-presenter to allocate surfaces.
old-location: dshow\ivmrsurfaceallocator9_initializedevice.htm
tech.root: DirectShow
ms.assetid: 44c22dc0-98a9-4a6e-a488-1d70dfff6acd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRSurfaceAllocator9 interface [DirectShow],InitializeDevice method, IVMRSurfaceAllocator9.InitializeDevice, IVMRSurfaceAllocator9::InitializeDevice, IVMRSurfaceAllocator9InitializeDevice, InitializeDevice, InitializeDevice method [DirectShow], InitializeDevice method [DirectShow],IVMRSurfaceAllocator9 interface, dshow.ivmrsurfaceallocator9_initializedevice, vmr9/IVMRSurfaceAllocator9::InitializeDevice
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
 - IVMRSurfaceAllocator9.InitializeDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRSurfaceAllocator9::InitializeDevice


## -description



The <b>InitializeDevice</b> method is called by the Video Mixing Renderer 9 (VMR-9) when it needs the allocator-presenter to allocate surfaces.




## -parameters




### -param dwUserID [in]

Application-defined identifier. This value is the same value that the application passed to the <a href="https://msdn.microsoft.com/99f9c549-e4b1-480b-97a4-7a29c9cdb649">IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator</a> method in the <i>dwUserID</i> parameter.


### -param lpAllocInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/d263b004-30e6-4dff-9df2-f4ca492f09f7">VMR9AllocationInfo</a> structure that contains a description of the surfaces to create.


### -param lpNumBuffers [in, out]

On input, specifies the number of surfaces to create. When the method returns, this parameter contains the number of buffers that were actually allocated.


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



Implement this method if you are providing a custom allocator-presenter for the VMR-9. You can use the <a href="https://msdn.microsoft.com/b69db9e9-6ab0-40ad-b929-30613c0b9e4b">IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper</a> method on the VMR-9 to allocate the surfaces.

Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/dd187168-19c7-414c-a764-f180d1d310f2">IVMRSurfaceAllocator9 Interface</a>



<a href="https://msdn.microsoft.com/19b43c9b-2578-418f-b03b-af7c7a3a46e4">Supplying a Custom Allocator-Presenter for VMR-7</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/0381f862-2f16-4b4d-be48-40f7fe151585">VMR Renderless Playback Mode (Custom Allocator-Presenters)</a>
 

 

