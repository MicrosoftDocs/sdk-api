---
UID: NF:vmr9.IVMRSurfaceAllocatorNotify9.ChangeD3DDevice
title: IVMRSurfaceAllocatorNotify9::ChangeD3DDevice
author: windows-sdk-content
description: The ChangeD3DDevice method notifies the VMR that the Direct3D device has changed.
old-location: dshow\ivmrsurfaceallocatornotify9_changed3ddevice.htm
tech.root: DirectShow
ms.assetid: 42199bdf-0cee-4dd0-98bc-66a8334b743b
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ChangeD3DDevice, ChangeD3DDevice method [DirectShow], ChangeD3DDevice method [DirectShow],IVMRSurfaceAllocatorNotify9 interface, IVMRSurfaceAllocatorNotify9 interface [DirectShow],ChangeD3DDevice method, IVMRSurfaceAllocatorNotify9.ChangeD3DDevice, IVMRSurfaceAllocatorNotify9::ChangeD3DDevice, IVMRSurfaceAllocatorNotify9ChangeD3DDevice, dshow.ivmrsurfaceallocatornotify9_changed3ddevice, vmr9/IVMRSurfaceAllocatorNotify9::ChangeD3DDevice
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
 - IVMRSurfaceAllocatorNotify9.ChangeD3DDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRSurfaceAllocatorNotify9::ChangeD3DDevice


## -description



The <code>ChangeD3DDevice</code> method notifies the VMR that the Direct3D device has changed.




## -parameters




### -param lpD3DDevice [in]

Pointer to the <b>IDirect3DDevice9</b> interface of the new device.


### -param hMonitor [in]

Handle to the monitor associated with the new device.


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




<a href="https://msdn.microsoft.com/f275b835-e5b3-46f4-8b26-a4b0e2554c7c">IVMRSurfaceAllocatorNotify9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

