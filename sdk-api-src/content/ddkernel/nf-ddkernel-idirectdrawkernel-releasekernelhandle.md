---
UID: NF:ddkernel.IDirectDrawKernel.ReleaseKernelHandle
title: IDirectDrawKernel::ReleaseKernelHandle (ddkernel.h)
description: The IDirectDrawKernel::ReleaseKernelHandle method releases a kernel-mode handle to the DirectDraw object.
helpviewer_keywords: ["IDirectDrawKernel interface [Display Devices]","ReleaseKernelHandle method","IDirectDrawKernel.ReleaseKernelHandle","IDirectDrawKernel::ReleaseKernelHandle","ReleaseKernelHandle","ReleaseKernelHandle method [Display Devices]","ReleaseKernelHandle method [Display Devices]","IDirectDrawKernel interface","ddfncs_5bb4adb5-8149-43bf-9a1a-b6447a68adac.xml","ddkernel/IDirectDrawKernel::ReleaseKernelHandle","display.idirectdrawkernel_releasekernelhandle"]
old-location: display\idirectdrawkernel_releasekernelhandle.htm
tech.root: display
ms.assetid: bbf3df75-f061-44d8-9ad4-e8524b6cb186
ms.date: 12/05/2018
ms.keywords: IDirectDrawKernel interface [Display Devices],ReleaseKernelHandle method, IDirectDrawKernel.ReleaseKernelHandle, IDirectDrawKernel::ReleaseKernelHandle, ReleaseKernelHandle, ReleaseKernelHandle method [Display Devices], ReleaseKernelHandle method [Display Devices],IDirectDrawKernel interface, ddfncs_5bb4adb5-8149-43bf-9a1a-b6447a68adac.xml, ddkernel/IDirectDrawKernel::ReleaseKernelHandle, display.idirectdrawkernel_releasekernelhandle
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
 - IDirectDrawKernel::ReleaseKernelHandle
 - ddkernel/IDirectDrawKernel::ReleaseKernelHandle
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
 - IDirectDrawKernel.ReleaseKernelHandle
---

# IDirectDrawKernel::ReleaseKernelHandle


## -description

The <b>IDirectDrawKernel::ReleaseKernelHandle</b> method releases a kernel-mode handle to the DirectDraw object.



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

