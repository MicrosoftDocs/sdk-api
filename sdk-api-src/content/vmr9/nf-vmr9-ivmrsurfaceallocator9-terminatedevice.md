---
UID: NF:vmr9.IVMRSurfaceAllocator9.TerminateDevice
title: IVMRSurfaceAllocator9::TerminateDevice
author: windows-sdk-content
description: The TerminateDevice method releases the Direct3D device.
old-location: dshow\ivmrsurfaceallocator9_terminatedevice.htm
tech.root: DirectShow
ms.assetid: 5006265d-6f2b-433b-b3ce-a7074d6eb159
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVMRSurfaceAllocator9 interface [DirectShow],TerminateDevice method, IVMRSurfaceAllocator9.TerminateDevice, IVMRSurfaceAllocator9::TerminateDevice, IVMRSurfaceAllocator9TerminateDevice, TerminateDevice, TerminateDevice method [DirectShow], TerminateDevice method [DirectShow],IVMRSurfaceAllocator9 interface, dshow.ivmrsurfaceallocator9_terminatedevice, vmr9/IVMRSurfaceAllocator9::TerminateDevice
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
 - IVMRSurfaceAllocator9.TerminateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vmr9.h
: 
- IVMRSurfaceAllocator9.TerminateDevice
: 
---

# IVMRSurfaceAllocator9::TerminateDevice


## -description



The <b>TerminateDevice</b> method releases the Direct3D device.




## -parameters




### -param dwID [in]

Application-defined identifier. This value is the same value that the application passed to the <a href="https://msdn.microsoft.com/99f9c549-e4b1-480b-97a4-7a29c9cdb649">IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator</a> method in the <i>dwUserID</i> parameter.


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
 

 

