---
UID: NF:vsprov.IVssProviderNotifications.OnLoad
title: IVssProviderNotifications::OnLoad
author: windows-sdk-content
description: Notifies a provider that it was loaded.
old-location: base\ivssprovidernotifications_onload.htm
tech.root: vss
ms.assetid: dd3df604-074b-4206-827e-3cc4d5f71f87
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVssProviderNotifications interface [VSS],OnLoad method, IVssProviderNotifications.OnLoad, IVssProviderNotifications::OnLoad, OnLoad, OnLoad method [VSS], OnLoad method [VSS],IVssProviderNotifications interface, base.ivssprovidernotifications_onload, vsprov/IVssProviderNotifications::OnLoad
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsProv.h
api_name:
 - IVssProviderNotifications.OnLoad
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<dt><b><b>S_OK</b></b></dt>
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
<dt><b><b>E_OUTOFMEMORY</b></b></dt>
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
<dt><b><b>VSS_E_PROVIDER_VETO</b></b></dt>
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




<a href="https://msdn.microsoft.com/09324f54-8902-43d1-a4f9-967adccbf8be">IVssProviderNotifications</a>



<a href="https://msdn.microsoft.com/5b9e0940-70b4-4913-9281-0347e60baa0d">OnUnload</a>
 

 

