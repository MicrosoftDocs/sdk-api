---
UID: NF:ddkernel.IDirectDrawSurfaceKernel.GetKernelHandle
title: IDirectDrawSurfaceKernel::GetKernelHandle (ddkernel.h)
description: The IDirectDrawSurfaceKernel::GetKernelHandle method returns a kernel-mode handle to the DirectDraw surface.
helpviewer_keywords: ["GetKernelHandle","GetKernelHandle method [Display Devices]","GetKernelHandle method [Display Devices]","IDirectDrawSurfaceKernel interface","IDirectDrawSurfaceKernel interface [Display Devices]","GetKernelHandle method","IDirectDrawSurfaceKernel.GetKernelHandle","IDirectDrawSurfaceKernel::GetKernelHandle","ddfncs_ae63c67e-aa40-4fb4-81c1-4659acb1319e.xml","ddkernel/IDirectDrawSurfaceKernel::GetKernelHandle","display.idirectdrawsurfacekernel_getkernelhandle"]
old-location: display\idirectdrawsurfacekernel_getkernelhandle.htm
tech.root: display
ms.assetid: 078af618-e393-4198-a181-89a6096f8aa8
ms.date: 12/05/2018
ms.keywords: GetKernelHandle, GetKernelHandle method [Display Devices], GetKernelHandle method [Display Devices],IDirectDrawSurfaceKernel interface, IDirectDrawSurfaceKernel interface [Display Devices],GetKernelHandle method, IDirectDrawSurfaceKernel.GetKernelHandle, IDirectDrawSurfaceKernel::GetKernelHandle, ddfncs_ae63c67e-aa40-4fb4-81c1-4659acb1319e.xml, ddkernel/IDirectDrawSurfaceKernel::GetKernelHandle, display.idirectdrawsurfacekernel_getkernelhandle
f1_keywords:
- ddkernel/IDirectDrawSurfaceKernel.GetKernelHandle
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ddkernel.h
api_name:
- IDirectDrawSurfaceKernel.GetKernelHandle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---


## -description


The <b>IDirectDrawSurfaceKernel::GetKernelHandle</b> method returns a kernel-mode handle to the DirectDraw surface.


## -parameters






#### -param unnamedParam1

Caller-supplied pointer into which the kernel-mode handle of the DirectDraw surface is returned.


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
 



