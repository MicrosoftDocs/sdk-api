---
UID: NF:comsvcs.IHolder.AllocResource
title: IHolder::AllocResource (comsvcs.h)
author: windows-sdk-content
description: Allocates a resource from the inventory.
old-location: cos\iholder_allocresource.htm
tech.root: cossdk
ms.assetid: 2b6c5d54-4917-460f-9740-abe4b578761f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AllocResource, AllocResource method [COM+], AllocResource method [COM+],IHolder interface, IHolder interface [COM+],AllocResource method, IHolder.AllocResource, IHolder::AllocResource, _dtc_IHolder_AllocResource, comsvcs/IHolder::AllocResource, cos.iholder_allocresource
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ComSvcs.h
api_name:
 - IHolder.AllocResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHolder::AllocResource


## -description


Allocates a resource from the inventory.


## -parameters




### -param __MIDL__IHolder0000 [in]

The type of resource to be allocated.


### -param __MIDL__IHolder0001 [out]

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
<i>ResTypId</i> is <b>NULL</b> or an empty string, or the Resource Dispenser's <a href="https://msdn.microsoft.com/en-us/library/ms684313(v=VS.85).aspx">IDispenserDriver::CreateResource</a> method generated an empty or duplicate RESID.

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
<li>Creates the resource by calling back to the Resource Dispenser's <a href="https://msdn.microsoft.com/en-us/library/ms684313(v=VS.85).aspx">IDispenserDriver::CreateResource</a> method, and then enlists it.</li>
</ol>
If the caller does not have a current transaction, the enlistment is skipped. Or if the Resource Dispenser rejects the enlistment (meaning the resource is not transaction capable), the enlistment is skipped.





## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>



<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>



<a href="https://msdn.microsoft.com/3c852e72-2fdc-4fd0-b523-f5601154da2a">IHolder</a>
 

 

