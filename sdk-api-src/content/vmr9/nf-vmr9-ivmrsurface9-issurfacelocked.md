---
UID: NF:vmr9.IVMRSurface9.IsSurfaceLocked
title: IVMRSurface9::IsSurfaceLocked (vmr9.h)
author: windows-sdk-content
description: The IsSurfaceLocked method indicates whether the Direct3D surface attached to this media sample is locked.
old-location: dshow\ivmrsurface9_issurfacelocked.htm
tech.root: DirectShow
ms.assetid: ccc2ab3c-ec6d-47b5-b6cf-0686aa4260bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRSurface9 interface [DirectShow],IsSurfaceLocked method, IVMRSurface9.IsSurfaceLocked, IVMRSurface9::IsSurfaceLocked, IVMRSurface9IsSurfaceLocked, IsSurfaceLocked, IsSurfaceLocked method [DirectShow], IsSurfaceLocked method [DirectShow],IVMRSurface9 interface, dshow.ivmrsurface9_issurfacelocked, vmr9/IVMRSurface9::IsSurfaceLocked
ms.topic: method
f1_keywords: ["vmr9/IVMRSurface9.IsSurfaceLocked"]
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
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrsurface9">IVMRSurface9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

