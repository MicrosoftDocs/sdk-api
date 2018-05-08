---
UID: NF:vmr9.IVMRSurfaceAllocatorNotify9.SetD3DDevice
title: IVMRSurfaceAllocatorNotify9::SetD3DDevice
author: windows-driver-content
description: The SetD3DDevice method sets the Direct3D device.
old-location: dshow\ivmrsurfaceallocatornotify9_setd3ddevice.htm
old-project: DirectShow
ms.assetid: f13fd7f4-03b3-4e10-9fe8-b81470b37253
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IVMRSurfaceAllocatorNotify9 interface [DirectShow],SetD3DDevice method, IVMRSurfaceAllocatorNotify9.SetD3DDevice, IVMRSurfaceAllocatorNotify9::SetD3DDevice, IVMRSurfaceAllocatorNotify9SetD3DDevice, SetD3DDevice, SetD3DDevice method [DirectShow], SetD3DDevice method [DirectShow],IVMRSurfaceAllocatorNotify9 interface, dshow.ivmrsurfaceallocatornotify9_setd3ddevice, vmr9/IVMRSurfaceAllocatorNotify9::SetD3DDevice
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
req.typenames: VMR9DeinterlaceTech
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRSurfaceAllocatorNotify9.SetD3DDevice
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRSurfaceAllocatorNotify9::SetD3DDevice


## -description



The <code>SetD3DDevice</code> method sets the Direct3D device.




## -parameters




### -param lpD3DDevice [in]

Pointer to the <b>IDirect3DDevice9</b> interface of the device.


### -param hMonitor [in]

Handle to a monitor.


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
 

 

