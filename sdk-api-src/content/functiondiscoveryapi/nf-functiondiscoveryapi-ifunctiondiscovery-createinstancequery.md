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

# IFunctionDiscovery::CreateInstanceQuery


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a query for a specific function instance.


## -parameters




### -param pszFunctionInstanceIdentity [in]

The identifier of the function instance.


### -param pIFunctionDiscoveryNotification [in]

A pointer to the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface implemented by the calling application. If specified, it enables the Function Discovery change notification process. This parameter can be <b>NULL</b>; however it is required for network providers.


### -param pfdqcQueryContext [in, out]

A pointer to the context in which the query was created. The type <b>FDQUERYCONTEXT</b> is defined as a DWORDLONG. 


### -param ppIFunctionInstanceQuery [out]

A pointer to an <a href="https://msdn.microsoft.com/03343d85-c0db-436d-bedc-c001b1886173">IFunctionInstanceQuery</a> interface pointer used to return the generated query.


## -returns



Possible return values include, but are not limited to, the following.

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
<i>ppIFunctionInstanceQuery</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
</table>
 




## -remarks



Function Discovery Network providers only return instances through the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface.

This method only initializes the query call. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff543208">Execute</a> method of the <a href="https://msdn.microsoft.com/03343d85-c0db-436d-bedc-c001b1886173">IFunctionInstanceQuery</a> interface returned in <i>ppIFunctionInstanceQuery</i> must be called to perform the query and return any data.




## -see-also




<a href="https://msdn.microsoft.com/3c255fb4-8f9d-47a2-9770-1aa528d07f43">Function Discovery Queries</a>



<a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a>
 

 

