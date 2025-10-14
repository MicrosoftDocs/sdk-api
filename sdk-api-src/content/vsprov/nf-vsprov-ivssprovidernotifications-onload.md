---
UID: NF:vsprov.IVssProviderNotifications.OnLoad
title: IVssProviderNotifications::OnLoad (vsprov.h)
description: Notifies a provider that it was loaded.
helpviewer_keywords: ["IVssProviderNotifications interface [VSS]","OnLoad method","IVssProviderNotifications.OnLoad","IVssProviderNotifications::OnLoad","OnLoad","OnLoad method [VSS]","OnLoad method [VSS]","IVssProviderNotifications interface","base.ivssprovidernotifications_onload","vsprov/IVssProviderNotifications::OnLoad"]
old-location: base\ivssprovidernotifications_onload.htm
tech.root: base
ms.assetid: dd3df604-074b-4206-827e-3cc4d5f71f87
ms.date: 12/05/2018
ms.keywords: IVssProviderNotifications interface [VSS],OnLoad method, IVssProviderNotifications.OnLoad, IVssProviderNotifications::OnLoad, OnLoad, OnLoad method [VSS], OnLoad method [VSS],IVssProviderNotifications interface, base.ivssprovidernotifications_onload, vsprov/IVssProviderNotifications::OnLoad
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVssProviderNotifications::OnLoad
 - vsprov/IVssProviderNotifications::OnLoad
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsProv.h
api_name:
 - IVssProviderNotifications.OnLoad
---

# IVssProviderNotifications::OnLoad


## -description

The <b>OnLoad</b> method 
  notifies a provider that it was loaded.

## -parameters

### -param pCallback [in]

This parameter is reserved.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>0x8007000EL</dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057L</dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
<dt>0x80042306L</dt>
</dl>
</td>
<td width="60%">
An unexpected provider error occurred. If this is returned, the error must be described in an entry in 
        the application event log, giving the user information on how to resolve the problem.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssprovidernotifications">IVssProviderNotifications</a>



<a href="/windows/desktop/api/vsprov/nf-vsprov-ivssprovidernotifications-onunload">OnUnload</a>