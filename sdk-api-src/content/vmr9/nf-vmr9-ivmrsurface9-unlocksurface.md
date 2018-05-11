---
UID: NF:vmr9.IVMRSurface9.UnlockSurface
title: IVMRSurface9::UnlockSurface
author: windows-driver-content
description: The UnlockSurface method unlocks the attached Direct3D surface.
old-location: dshow\ivmrsurface9_unlocksurface.htm
old-project: DirectShow
ms.assetid: 2785b1b7-62ed-420d-ab98-264e1b03b578
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IVMRSurface9 interface [DirectShow],UnlockSurface method, IVMRSurface9.UnlockSurface, IVMRSurface9::UnlockSurface, IVMRSurface9UnlockSurface, UnlockSurface, UnlockSurface method [DirectShow], UnlockSurface method [DirectShow],IVMRSurface9 interface, dshow.ivmrsurface9_unlocksurface, vmr9/IVMRSurface9::UnlockSurface
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
-	IVMRSurface9.UnlockSurface
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRSurface9::UnlockSurface


## -description



The <code>UnlockSurface</code> method unlocks the attached Direct3D surface.




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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No Direct3D surface is attached to this sample.

</td>
</tr>
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/b24dae7d-5e88-4973-8507-8bd13cdccbde">IVMRSurface9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

