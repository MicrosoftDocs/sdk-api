---
UID: NF:ddkernel.IDirectDrawSurfaceKernel.ReleaseKernelHandle
title: IDirectDrawSurfaceKernel::ReleaseKernelHandle
author: windows-sdk-content
description: The IDirectDrawSurfaceKernel::ReleaseKernelHandle method releases a kernel-mode handle to the DirectDraw surface.
old-location: display\idirectdrawsurfacekernel_releasekernelhandle.htm
old-project: display
ms.assetid: 75110b32-0b20-4d2a-8988-d4263fdabb46
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: IDirectDrawSurfaceKernel interface [Display Devices],ReleaseKernelHandle method, IDirectDrawSurfaceKernel.ReleaseKernelHandle, IDirectDrawSurfaceKernel::ReleaseKernelHandle, ReleaseKernelHandle, ReleaseKernelHandle method [Display Devices], ReleaseKernelHandle method [Display Devices],IDirectDrawSurfaceKernel interface, ddfncs_f952a7c7-399d-4de3-8351-b44a79c34c09.xml, ddkernel/IDirectDrawSurfaceKernel::ReleaseKernelHandle, display.idirectdrawsurfacekernel_releasekernelhandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MONMSGSTRUCT, *PMONMSGSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ddkernel.h
api_name:
 - IDirectDrawSurfaceKernel.ReleaseKernelHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectDrawSurfaceKernel::ReleaseKernelHandle


## -description


The <b>IDirectDrawSurfaceKernel::ReleaseKernelHandle</b> method releases a kernel-mode handle to the DirectDraw surface.


## -parameters






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
 



