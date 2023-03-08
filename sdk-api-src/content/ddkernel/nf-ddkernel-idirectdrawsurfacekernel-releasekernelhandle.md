---
UID: NF:ddkernel.IDirectDrawSurfaceKernel.ReleaseKernelHandle
title: IDirectDrawSurfaceKernel::ReleaseKernelHandle (ddkernel.h)
description: The IDirectDrawSurfaceKernel::ReleaseKernelHandle method releases a kernel-mode handle to the DirectDraw surface.
helpviewer_keywords: ["IDirectDrawSurfaceKernel interface [Display Devices]","ReleaseKernelHandle method","IDirectDrawSurfaceKernel.ReleaseKernelHandle","IDirectDrawSurfaceKernel::ReleaseKernelHandle","ReleaseKernelHandle","ReleaseKernelHandle method [Display Devices]","ReleaseKernelHandle method [Display Devices]","IDirectDrawSurfaceKernel interface","ddfncs_f952a7c7-399d-4de3-8351-b44a79c34c09.xml","ddkernel/IDirectDrawSurfaceKernel::ReleaseKernelHandle","display.idirectdrawsurfacekernel_releasekernelhandle"]
old-location: display\idirectdrawsurfacekernel_releasekernelhandle.htm
tech.root: display
ms.assetid: 75110b32-0b20-4d2a-8988-d4263fdabb46
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurfaceKernel interface [Display Devices],ReleaseKernelHandle method, IDirectDrawSurfaceKernel.ReleaseKernelHandle, IDirectDrawSurfaceKernel::ReleaseKernelHandle, ReleaseKernelHandle, ReleaseKernelHandle method [Display Devices], ReleaseKernelHandle method [Display Devices],IDirectDrawSurfaceKernel interface, ddfncs_f952a7c7-399d-4de3-8351-b44a79c34c09.xml, ddkernel/IDirectDrawSurfaceKernel::ReleaseKernelHandle, display.idirectdrawsurfacekernel_releasekernelhandle
req.header: ddkernel.h
req.include-header: Ddkernel.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawSurfaceKernel::ReleaseKernelHandle
 - ddkernel/IDirectDrawSurfaceKernel::ReleaseKernelHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ddkernel.h
api_name:
 - IDirectDrawSurfaceKernel.ReleaseKernelHandle
---

# IDirectDrawSurfaceKernel::ReleaseKernelHandle


## -description

The <b>IDirectDrawSurfaceKernel::ReleaseKernelHandle</b> method releases a kernel-mode handle to the DirectDraw surface.



## -returns

The method must return one of the following values:

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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented.

</td>
</tr>
</table>

