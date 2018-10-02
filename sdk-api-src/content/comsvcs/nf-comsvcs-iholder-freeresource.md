---
UID: NF:comsvcs.IHolder.FreeResource
title: IHolder::FreeResource
author: windows-sdk-content
description: Returns a resource to the inventory.
old-location: cos\iholder_freeresource.htm
tech.root: cossdk
ms.assetid: 1d110bf6-7204-4fbb-abb7-ced7cf885e5b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FreeResource, FreeResource method [COM+], FreeResource method [COM+],IHolder interface, IHolder interface [COM+],FreeResource method, IHolder.FreeResource, IHolder::FreeResource, _dtc_IHolder_FreeResource, comsvcs/IHolder::FreeResource, cos.iholder_freeresource
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IHolder.FreeResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHolder::FreeResource


## -description


Returns a resource to the inventory.


## -parameters




### -param __MIDL__IHolder0002

TBD




#### - ResId [in]

The handle of the resource to be freed.


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
<i>ResTypId</i> is not a valid resource handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL </b></dt>
</dl>
</td>
<td width="60%">
The method failed. The resource has not been freed.

</td>
</tr>
</table>
 




## -remarks



A resource originally returned by <a href="https://msdn.microsoft.com/2b6c5d54-4917-460f-9740-abe4b578761f">IHolder::AllocResource</a> is returned to the pool. This notifies the Resource Dispenser through <a href="https://msdn.microsoft.com/59df0703-90ea-480c-8608-7d43039b48ba">IDispenserDriver::ResetResource</a>, which is the Resource Dispenser's opportunity to prepare the resource before it is returned to the pool.





## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>



<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>



<a href="https://msdn.microsoft.com/3c852e72-2fdc-4fd0-b523-f5601154da2a">IHolder</a>
 

 

