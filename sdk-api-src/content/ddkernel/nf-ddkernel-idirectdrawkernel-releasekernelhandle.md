---
UID: NF:ddkernel.IDirectDrawKernel.ReleaseKernelHandle
title: IDirectDrawKernel::ReleaseKernelHandle
author: windows-driver-content
description: The IDirectDrawKernel::ReleaseKernelHandle method releases a kernel-mode handle to the DirectDraw object.
old-location: display\idirectdrawkernel_releasekernelhandle.htm
old-project: display
ms.assetid: bbf3df75-f061-44d8-9ad4-e8524b6cb186
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IDirectDrawKernel interface [Display Devices],ReleaseKernelHandle method, IDirectDrawKernel.ReleaseKernelHandle, IDirectDrawKernel::ReleaseKernelHandle, ReleaseKernelHandle, ReleaseKernelHandle method [Display Devices], ReleaseKernelHandle method [Display Devices],IDirectDrawKernel interface, ddfncs_5bb4adb5-8149-43bf-9a1a-b6447a68adac.xml, ddkernel/IDirectDrawKernel::ReleaseKernelHandle, display.idirectdrawkernel_releasekernelhandle
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MONMSGSTRUCT, *PMONMSGSTRUCT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ddkernel.h
api_name:
-	IDirectDrawKernel.ReleaseKernelHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectDrawKernel::ReleaseKernelHandle


## -description


The <b>IDirectDrawKernel::ReleaseKernelHandle</b> method releases a kernel-mode handle to the DirectDraw object.


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
 



