---
UID: NF:ddkernel.IDirectDrawKernel.GetCaps
title: IDirectDrawKernel::GetCaps
author: windows-sdk-content
description: The IDirectDrawKernel::GetCaps method returns the capabilities of this kernel-mode device.
old-location: display\idirectdrawkernel_getcaps.htm
old-project: display
ms.assetid: c97ebe38-d62c-4ce8-8530-193dd83ef3d4
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetCaps, GetCaps method [Display Devices], GetCaps method [Display Devices],IDirectDrawKernel interface, IDirectDrawKernel interface [Display Devices],GetCaps method, IDirectDrawKernel.GetCaps, IDirectDrawKernel::GetCaps, ddfncs_52bda933-e948-4942-b52b-c0a42440c1fb.xml, ddkernel/IDirectDrawKernel::GetCaps, display.idirectdrawkernel_getcaps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddkernel.h
req.include-header: Ddraw.h, Ddkernel.h, Winddi.h
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
-	IDirectDrawKernel.GetCaps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectDrawKernel::GetCaps


## -description


The <b>IDirectDrawKernel::GetCaps</b> method returns the capabilities of this kernel-mode device.


## -parameters






#### - lpCaps

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549593">DDKERNELCAPS</a> structure into which the kernel-mode capabilities of the DirectDraw device are returned.


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
 



