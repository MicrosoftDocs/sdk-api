---
UID: NF:vmr9.IVMRSurface9.GetSurface
title: IVMRSurface9::GetSurface (vmr9.h)
description: The GetSurface method retrieves the attached Direct3D surface.helpviewer_keywords: ["GetSurface","GetSurface method [DirectShow]","GetSurface method [DirectShow]","IVMRSurface9 interface","IVMRSurface9 interface [DirectShow]","GetSurface method","IVMRSurface9.GetSurface","IVMRSurface9::GetSurface","IVMRSurface9GetSurface","dshow.ivmrsurface9_getsurface","vmr9/IVMRSurface9::GetSurface"]
old-location: dshow\ivmrsurface9_getsurface.htm
tech.root: DirectShow
ms.assetid: ce556b66-0a28-43a0-9dd2-a1c3b9aad5dc
ms.date: 12/05/2018
ms.keywords: GetSurface, GetSurface method [DirectShow], GetSurface method [DirectShow],IVMRSurface9 interface, IVMRSurface9 interface [DirectShow],GetSurface method, IVMRSurface9.GetSurface, IVMRSurface9::GetSurface, IVMRSurface9GetSurface, dshow.ivmrsurface9_getsurface, vmr9/IVMRSurface9::GetSurface
f1_keywords:
- vmr9/IVMRSurface9.GetSurface
dev_langs:
- c++
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
- IVMRSurface9.GetSurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurface9::GetSurface


## -description



The <code>GetSurface</code> method retrieves the attached Direct3D surface.




## -parameters




### -param lplpSurface [out]

Address of a variable that receives an <b>IDirect3DSurface9</b> interface pointer. The caller must release the interface.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>lplpSurface</i> is invalid.

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



The media sample object increments the reference count on the returned interface. The caller must call Release on the interface.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrsurface9">IVMRSurface9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

