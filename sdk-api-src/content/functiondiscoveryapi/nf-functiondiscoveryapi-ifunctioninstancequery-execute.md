---
UID: NF:functiondiscoveryapi.IFunctionInstanceQuery.Execute
title: IFunctionInstanceQuery::Execute
author: windows-sdk-content
description: Performs the query defined by IFunctionDiscovery::CreateInstanceQuery.
old-location: ncd\ifunctioninstancequery_execute_method.htm
tech.root: fundisc
ms.assetid: 42618944-6ae6-45f0-85f9-3c958d719ed2
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Execute, Execute method, Execute method,IFunctionInstanceQuery interface, IFunctionInstanceQuery interface,Execute method, IFunctionInstanceQuery.Execute, IFunctionInstanceQuery::Execute, functiondiscoveryapi/IFunctionInstanceQuery::Execute, ncd.ifunctioninstancequery_execute_method
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: FunDisc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstanceQuery.Execute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionInstanceQuery::Execute


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Performs the query defined by <a href="https://msdn.microsoft.com/80e70972-ced1-416e-aa4f-69c54b2cbf95">IFunctionDiscovery::CreateInstanceQuery</a>. 


## -parameters




### -param ppIFunctionInstance [out]

A pointer to an <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface pointer that receives the requested function instance.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code/value</th>
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
The <i>ppIFunctionInstance</i> parameter is <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The results to be returned by a provider will come through asynchronous notification.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_OBJECT_NOT_FOUND)</b></dt>
<dt>0x800710d8</dt>
</dl>
</td>
<td width="60%">
The function instance represented by the specified ID does not exist on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_KEY_DELETED)</b></dt>
<dt>0x800703fa</dt>
</dl>
</td>
<td width="60%">
The function instance could not be returned because the key corresponding to the function instance was deleted by another process. This error is returned by the registry provider if a key is deleted while query processing is taking place.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
<dt>0x80070002</dt>
</dl>
</td>
<td width="60%">
The function instance could not be returned because the key corresponding to the function instance could not be found. This error is returned by the registry provider when the provider could not find matching instances for an instance query.

</td>
</tr>
</table>
 

A predefined query is a query of a layered <a href="https://msdn.microsoft.com/476df2f0-6ed0-4275-90e7-752d7279bf1b">category</a>. When a predefined query is executed, each provider that returns a function instance also returns an HRESULT value. The provider HRESULT values  are aggregated, and the value returned by the <a href="https://msdn.microsoft.com/b924d066-87d7-499b-b006-a10e219e11fd">Execute</a>  method reflects these aggregate results. Results are aggregated as follows:

<ul>
<li>If all providers return S_OK, <a href="https://msdn.microsoft.com/b924d066-87d7-499b-b006-a10e219e11fd">Execute</a>   returns S_OK.</li>
<li>If at least one provider returns E_PENDING, and all other providers return either S_OK or E_PENDING, <a href="https://msdn.microsoft.com/b924d066-87d7-499b-b006-a10e219e11fd">Execute</a>   returns E_PENDING.</li>
<li>If all providers return an error value (that is, a value other than S_OK or E_PENDING), <a href="https://msdn.microsoft.com/b924d066-87d7-499b-b006-a10e219e11fd">Execute</a> returns the error value returned by the network provider that was last queried. Also, if the client's  <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> callback routine was provided to <a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">IFunctionDiscovery::CreateInstanceCollectionQuery</a>, an <a href="https://msdn.microsoft.com/c4dcc4e9-7acf-44d3-b337-1ac01afa19b0">OnError</a>  notification is sent for each provider. Each   <b>OnError</b> notification contains the HRESULT returned by the provider.</li>
<li>If at least one provider returns an error value, and all other providers return S_OK, <a href="https://msdn.microsoft.com/b924d066-87d7-499b-b006-a10e219e11fd">Execute</a>   returns S_OK. <a href="https://msdn.microsoft.com/c4dcc4e9-7acf-44d3-b337-1ac01afa19b0">OnError</a>  notification(s) are sent as described above.</li>
<li>If at least one provider returns an error value, and at least one provider returns E_PENDING, <a href="https://msdn.microsoft.com/b924d066-87d7-499b-b006-a10e219e11fd">Execute</a> returns E_PENDING.  <a href="https://msdn.microsoft.com/c4dcc4e9-7acf-44d3-b337-1ac01afa19b0">OnError</a> notification(s) are sent as described above.</li>
</ul>



## -remarks



This method must be must be invoked by the client program to retrieve data from the query object. When called, this method performs the following: 

<ol>
<li>Retrieves the function instance.</li>
<li>Initiates the update notification mechanism if the address of the client program's <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> callback routine is provided to <a href="https://msdn.microsoft.com/80e70972-ced1-416e-aa4f-69c54b2cbf95">IFunctionDiscovery::CreateInstanceQuery</a>.</li>
</ol>
Function Discovery network providers only return function instances through the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface.  They return no function instances directly when this method is invoked. Instead, <b>Execute</b> simply initiates an entirely asynchronous retrieval operation and returns E_PENDING to indicate that the results will be returned asynchronously.   Notifications must be used to retrieve function instances from Function Discovery network providers.

If <b>Execute</b> is called twice on the same query object, the first query is terminated before the second query executes. 




## -see-also




<a href="https://msdn.microsoft.com/3c255fb4-8f9d-47a2-9770-1aa528d07f43">Function Discovery Queries</a>



<a href="https://msdn.microsoft.com/03343d85-c0db-436d-bedc-c001b1886173">IFunctionInstanceQuery</a>
 

 

