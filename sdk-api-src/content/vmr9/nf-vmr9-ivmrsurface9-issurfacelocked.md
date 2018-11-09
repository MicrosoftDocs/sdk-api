---
UID: NF:vmr9.IVMRSurface9.IsSurfaceLocked
title: IVMRSurface9::IsSurfaceLocked
author: windows-sdk-content
description: The IsSurfaceLocked method indicates whether the Direct3D surface attached to this media sample is locked.
old-location: dshow\ivmrsurface9_issurfacelocked.htm
tech.root: DirectShow
ms.assetid: ccc2ab3c-ec6d-47b5-b6cf-0686aa4260bc
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRSurface9 interface [DirectShow],IsSurfaceLocked method, IVMRSurface9.IsSurfaceLocked, IVMRSurface9::IsSurfaceLocked, IVMRSurface9IsSurfaceLocked, IsSurfaceLocked, IsSurfaceLocked method [DirectShow], IsSurfaceLocked method [DirectShow],IVMRSurface9 interface, dshow.ivmrsurface9_issurfacelocked, vmr9/IVMRSurface9::IsSurfaceLocked
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
 - IVMRSurface9.IsSurfaceLocked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRSurface9::IsSurfaceLocked


## -description



The <code>IsSurfaceLocked</code> method indicates whether the Direct3D surface attached to this media sample is locked.




## -parameters






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




<a href="https://msdn.microsoft.com/b24dae7d-5e88-4973-8507-8bd13cdccbde">IVMRSurface9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

