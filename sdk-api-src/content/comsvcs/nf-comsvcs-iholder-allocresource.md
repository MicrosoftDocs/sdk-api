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

# IHolder::AllocResource


## -description


Allocates a resource from the inventory.


## -parameters




### -param __MIDL__IHolder0000




### -param __MIDL__IHolder0001






#### - ResTypId [in]

The type of resource to be allocated.


#### - pResId [out]

A pointer to the location where the handle of the allocated resource is returned.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ResTypId</i> is <b>NULL</b> or an empty string, or the Resource Dispenser's <a href="https://msdn.microsoft.com/97b49069-3428-48da-a818-737f3bc342d0">IDispenserDriver::CreateResource</a> method generated an empty or duplicate RESID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL </b></dt>
</dl>
</td>
<td width="60%">
The method failed. The <i>pResId</i> parameter has not been set. The likely cause is that the caller's transaction is aborting.

</td>
</tr>
</table>
 




## -remarks



The Dispenser Manager takes the following steps to locate a resource:

<ol>
<li>Searches the pool for a free resource of this RESTYPID, which is already enlisted in the caller's current transaction.</li>
<li>Searches the pool for a free unenlisted resource of this RESTYPID, and then enlists it in the caller's current transaction.</li>
<li>Creates the resource by calling back to the Resource Dispenser's <a href="https://msdn.microsoft.com/97b49069-3428-48da-a818-737f3bc342d0">IDispenserDriver::CreateResource</a> method, and then enlists it.</li>
</ol>
If the caller does not have a current transaction, the enlistment is skipped. Or if the Resource Dispenser rejects the enlistment (meaning the resource is not transaction capable), the enlistment is skipped.





## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>



<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>



<a href="https://msdn.microsoft.com/3c852e72-2fdc-4fd0-b523-f5601154da2a">IHolder</a>
 

 

