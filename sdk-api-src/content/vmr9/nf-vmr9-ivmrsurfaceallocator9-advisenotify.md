---
UID: NF:vmr9.IVMRSurfaceAllocator9.AdviseNotify
title: IVMRSurfaceAllocator9::AdviseNotify
author: windows-sdk-content
description: The AdviseNotify method provides the allocator-presenter with the VMR-9 filter's interface for notification callbacks.
old-location: dshow\ivmrsurfaceallocator9_advisenotify.htm
tech.root: DirectShow
ms.assetid: 2c367444-50bf-4fbe-b2d9-ed32275576e9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AdviseNotify, AdviseNotify method [DirectShow], AdviseNotify method [DirectShow],IVMRSurfaceAllocator9 interface, IVMRSurfaceAllocator9 interface [DirectShow],AdviseNotify method, IVMRSurfaceAllocator9.AdviseNotify, IVMRSurfaceAllocator9::AdviseNotify, IVMRSurfaceAllocator9AdviseNotify, dshow.ivmrsurfaceallocator9_advisenotify, vmr9/IVMRSurfaceAllocator9::AdviseNotify
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
 - IVMRSurfaceAllocator9.AdviseNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRSurfaceAllocator9::AdviseNotify


## -description



The <b>AdviseNotify</b> method provides the allocator-presenter with the VMR-9 filter's interface for notification callbacks. If you are using a custom allocator-presenter, the application must call this method on the allocator-presenter, with a pointer to the VMR's <a href="https://msdn.microsoft.com/f275b835-e5b3-46f4-8b26-a4b0e2554c7c">IVMRSurfaceAllocatorNotify9</a> interface. The allocator-presenter uses this interface to communicate with the VMR.



If you are not using a custom allocator-presenter, the application does not have to call this method.


## -parameters




### -param lpIVMRSurfAllocNotify [in]

Specifies the <a href="https://msdn.microsoft.com/f275b835-e5b3-46f4-8b26-a4b0e2554c7c">IVMRSurfaceAllocatorNotify9</a> interface that the allocator-presenter will use to pass notifications back to the VMR.


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



<a href="https://msdn.microsoft.com/19b43c9b-2578-418f-b03b-af7c7a3a46e4">Supplying a Custom Allocator-Presenter for VMR-7</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/0381f862-2f16-4b4d-be48-40f7fe151585">VMR Renderless Playback Mode (Custom Allocator-Presenters)</a>
 

 

