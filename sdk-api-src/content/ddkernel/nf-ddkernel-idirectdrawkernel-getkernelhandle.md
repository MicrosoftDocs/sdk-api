---
UID: NF:ddkernel.IDirectDrawKernel.GetKernelHandle
title: IDirectDrawKernel::GetKernelHandle (ddkernel.h)
description: The IDirectDrawKernel::GetKernelHandle method returns a kernel-mode handle to the DirectDraw object.
helpviewer_keywords: ["GetKernelHandle","GetKernelHandle method [Display Devices]","GetKernelHandle method [Display Devices]","IDirectDrawKernel interface","IDirectDrawKernel interface [Display Devices]","GetKernelHandle method","IDirectDrawKernel.GetKernelHandle","IDirectDrawKernel::GetKernelHandle","ddfncs_5c255735-5359-481b-b6cb-3bae2d934926.xml","ddkernel/IDirectDrawKernel::GetKernelHandle","display.idirectdrawkernel_getkernelhandle"]
old-location: display\idirectdrawkernel_getkernelhandle.htm
tech.root: display
ms.assetid: f74cc859-6991-4075-a7ef-83a67de06be6
ms.date: 12/05/2018
ms.keywords: GetKernelHandle, GetKernelHandle method [Display Devices], GetKernelHandle method [Display Devices],IDirectDrawKernel interface, IDirectDrawKernel interface [Display Devices],GetKernelHandle method, IDirectDrawKernel.GetKernelHandle, IDirectDrawKernel::GetKernelHandle, ddfncs_5c255735-5359-481b-b6cb-3bae2d934926.xml, ddkernel/IDirectDrawKernel::GetKernelHandle, display.idirectdrawkernel_getkernelhandle
f1_keywords:
- ddkernel/IDirectDrawKernel.GetKernelHandle
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
- IDirectDrawKernel.GetKernelHandle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---



## -description


The <b>IDirectDrawKernel::GetKernelHandle</b> method returns a kernel-mode handle to the DirectDraw object.


## -parameters






#### -param unnamedParam1

Caller-supplied pointer into which the kernel-mode handle of the DirectDraw object is returned.


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
 



