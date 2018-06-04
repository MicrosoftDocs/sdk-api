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
 

 

