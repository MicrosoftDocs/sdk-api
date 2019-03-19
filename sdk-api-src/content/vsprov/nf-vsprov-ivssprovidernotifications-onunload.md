---
UID: NF:vsprov.IVssProviderNotifications.OnUnload
title: IVssProviderNotifications::OnUnload (vsprov.h)
author: windows-sdk-content
description: Notifies the provider to prepare to be unloaded.
old-location: base\ivssprovidernotifications_onunload.htm
tech.root: VSS
ms.assetid: 5b9e0940-70b4-4913-9281-0347e60baa0d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVssProviderNotifications interface [VSS],OnUnload method, IVssProviderNotifications.OnUnload, IVssProviderNotifications::OnUnload, OnUnload, OnUnload method [VSS], OnUnload method [VSS],IVssProviderNotifications interface, base.ivssprovidernotifications_onunload, vsprov/IVssProviderNotifications::OnUnload
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
 - IVssProviderNotifications.OnUnload
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssProviderNotifications::OnUnload


## -description


The <b>OnUnload</b> method 
  notifies the provider  to prepare to be unloaded.


## -parameters




### -param bForceUnload [in]

If <b>TRUE</b>, the provider must prepare to be released.


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
There are no pending operations and the  provider is ready to be released.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The provider should not be unloaded. This value can only be returned if <i>bForceUnload</i> is <b>FALSE</b>.

</td>
</tr>
</table>
 




## -remarks



If <i>bForceUnload</i> is <b>TRUE</b>, the return value must be 
   <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/09324f54-8902-43d1-a4f9-967adccbf8be">IVssProviderNotifications</a>



<a href="https://msdn.microsoft.com/dd3df604-074b-4206-827e-3cc4d5f71f87">OnLoad</a>
 

 

