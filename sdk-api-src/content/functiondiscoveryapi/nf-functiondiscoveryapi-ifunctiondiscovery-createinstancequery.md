---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.CreateInstanceQuery
title: IFunctionDiscovery::CreateInstanceQuery
author: windows-sdk-content
description: Creates a query for a specific function instance.
old-location: ncd\ifunctiondiscovery_createinstancequery_method.htm
old-project: fundisc
ms.assetid: 80e70972-ced1-416e-aa4f-69c54b2cbf95
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: CreateInstanceQuery, CreateInstanceQuery method, CreateInstanceQuery method,IFunctionDiscovery interface, IFunctionDiscovery interface,CreateInstanceQuery method, IFunctionDiscovery.CreateInstanceQuery, IFunctionDiscovery::CreateInstanceQuery, functiondiscoveryapi/IFunctionDiscovery::CreateInstanceQuery, ncd.ifunctiondiscovery_createinstancequery_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SystemVisibilityFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionDiscovery.CreateInstanceQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: FunDisc.dll
req.irql: 
req.product: Internet Explorer 5
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
 

 

