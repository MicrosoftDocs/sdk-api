---
UID: NF:ddkernel.IDirectDrawKernel.GetCaps
title: IDirectDrawKernel::GetCaps (ddkernel.h)
description: The IDirectDrawKernel::GetCaps method returns the capabilities of this kernel-mode device.
helpviewer_keywords: ["GetCaps","GetCaps method [Display Devices]","GetCaps method [Display Devices]","IDirectDrawKernel interface","IDirectDrawKernel interface [Display Devices]","GetCaps method","IDirectDrawKernel.GetCaps","IDirectDrawKernel::GetCaps","ddfncs_52bda933-e948-4942-b52b-c0a42440c1fb.xml","ddkernel/IDirectDrawKernel::GetCaps","display.idirectdrawkernel_getcaps"]
old-location: display\idirectdrawkernel_getcaps.htm
tech.root: display
ms.assetid: c97ebe38-d62c-4ce8-8530-193dd83ef3d4
ms.date: 12/05/2018
ms.keywords: GetCaps, GetCaps method [Display Devices], GetCaps method [Display Devices],IDirectDrawKernel interface, IDirectDrawKernel interface [Display Devices],GetCaps method, IDirectDrawKernel.GetCaps, IDirectDrawKernel::GetCaps, ddfncs_52bda933-e948-4942-b52b-c0a42440c1fb.xml, ddkernel/IDirectDrawKernel::GetCaps, display.idirectdrawkernel_getcaps
f1_keywords:
- ddkernel/IDirectDrawKernel.GetCaps
dev_langs:
- c++
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
- IDirectDrawKernel.GetCaps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

The <b>IDirectDrawKernel::GetCaps</b> method returns the capabilities of this kernel-mode device.

## -parameters

#### -param unnamedParam1

Caller-supplied pointer to a <a href="/windows/desktop/api/ddkernel/ns-ddkernel-ddkernelcaps">DDKERNELCAPS</a> structure into which the kernel-mode capabilities of the DirectDraw device are returned.

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