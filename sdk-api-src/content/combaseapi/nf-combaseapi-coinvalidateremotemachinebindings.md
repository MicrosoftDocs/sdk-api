---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# CoInvalidateRemoteMachineBindings function


## -description


Tells the <a href="https://msdn.microsoft.com/56ad011d-17c4-4410-b598-6ef47fb3638f">service control manager</a> to flush any cached RPC binding handles for the specified computer.

Only administrators may call this function.


## -parameters




### -param pszMachineName [in]

The computer name for which binding handles should be flushed, or an empty string to signify that all handles in the cache should be flushed.


## -returns



This function can return the following values.

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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_S_MACHINENAMENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the specified computer name was not found or that the binding handle cache was empty, indicating that an empty string was passed instead of a specific computer name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Indicates the caller was not an administrator for this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a <b>NULL</b> value was passed for <i>pszMachineName</i>.


</td>
</tr>
</table>
 




## -remarks



The OLE Service Control Manager is used by COM to send component activation requests to other machines. To do this, the OLE Service Control Manager maintains a cache of RPC binding handles to send activation requests to computer, keyed by computer name. Under normal circumstances, this works well, but in some scenarios, such as Web farms and load-balancing situations, the ability to purge this cache of specific handles might be needed in order to facilitate rebinding to a different physical server by the same name. <b>CoInvalidateRemoteMachineBindings</b> is used for this purpose.

The OLE Service Control Manager will flush unused binding handles over time. It is not necessary to call <b>CoInvalidateRemoteMachineBindings</b> to do this.



