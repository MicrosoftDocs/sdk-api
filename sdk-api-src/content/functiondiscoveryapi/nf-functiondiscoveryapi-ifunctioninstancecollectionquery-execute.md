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

# IFunctionInstanceCollectionQuery::Execute


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Performs the query defined by <a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">IFunctionDiscovery::CreateInstanceCollectionQuery</a>.


## -parameters




### -param ppIFunctionInstanceCollection [out]

A pointer to an <a href="https://msdn.microsoft.com/8ac1a406-92f3-4e39-985e-ab8fa7d28751">IFunctionInstanceCollection</a> interface pointer that receives the requested function instance collection.


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
The method completed successfully.   Results are returned synchronously in <i>ppIFunctonInstanceCollecton</i>.

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
Some of the results will be returned by asynchronous notification.  See the remarks for details.

</td>
</tr>
</table>
 

 A predefined query is a query of a layered <a href="https://msdn.microsoft.com/476df2f0-6ed0-4275-90e7-752d7279bf1b">category</a>. When a predefined query is executed, each provider that returns a function instance also returns an HRESULT value. The provider HRESULT values  are aggregated, and the value returned by the <b>Execute</b>  method reflects these aggregate results. Results are aggregated as follows:

<ul>
<li>If all providers return <b>S_OK</b>, <b>Execute</b>   returns <b>S_OK</b>.</li>
<li>If at least one provider returns <b>E_PENDING</b>, and all other providers return either <b>S_OK</b> or <b>E_PENDING</b>, <b>Execute</b>   returns <b>E_PENDING</b>.</li>
<li>If all providers return an error value (that is, a value other than <b>S_OK</b> or <b>E_PENDING</b>), <b>Execute</b> returns the error value returned by the network provider that was last queried. Also, if the client's  <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> callback routine was provided to <a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">IFunctionDiscovery::CreateInstanceCollectionQuery</a>, an <a href="https://msdn.microsoft.com/c4dcc4e9-7acf-44d3-b337-1ac01afa19b0">OnError</a>  notification is sent for each provider. Each   <b>OnError</b> notification contains the HRESULT returned by the provider.</li>
<li>If at least one provider returns an error value, and all other providers return <b>S_OK</b>, <b>Execute</b>   returns <b>S_OK</b>. <a href="https://msdn.microsoft.com/c4dcc4e9-7acf-44d3-b337-1ac01afa19b0">OnError</a>  notifications are sent as described above.</li>
<li>If at least one provider returns an error value, and at least one provider returns <b>E_PENDING</b>, <b>Execute</b> returns <b>E_PENDING</b>.  <a href="https://msdn.microsoft.com/c4dcc4e9-7acf-44d3-b337-1ac01afa19b0">OnError</a> notifications are sent as described above.</li>
</ul>
When <b>Execute</b> returns <b>S_OK</b>, <i>ppIFunctionInstanceCollection</i> contains the results of the query.  If an <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface is provided to the <a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">CreateInstanceCollectionQuery</a> method of  <a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a>, then changes to the results will be communicated using that interface.

When <b>Execute</b> returns <b>E_PENDING</b>, the result set will be returned asynchronously through the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface provided to the <a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">CreateInstanceCollectionQuery</a> method of <a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a>.  <i>ppIFunctionInstanceCollection</i> may be <b>NULL</b> or may contain a partial result set.  The enumeration is complete once the <a href="https://msdn.microsoft.com/4ebfdf15-ca37-4905-b842-8854a0bd276b">OnEvent</a> method of  <b>IFunctionDiscoveryNotification</b> is called with <b>FD_EVENTID_SEARCHCOMPLETE</b>.  After the <b>FD_EVENTID_SEARCHCOMPLETE</b> event is received, additional notifications are updates to the results.




## -remarks



This method must be must be invoked by the client program before any data can be retrieved from the query object. When called, this method performs the following: 

<ol>
<li>Retrieves the function instance collection object.</li>
<li>Queries the provider of the category that is passed into <a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">IFunctionDiscovery::CreateInstanceCollectionQuery</a>.</li>
<li>Retrieves the category provider.</li>
<li>Queries the category provider  using the subcategory data to generate the collection using query constraints.</li>
<li>Initiates the update notification mechanism if the address of the client program's <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> callback routine is provided to <a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">IFunctionDiscovery::CreateInstanceCollectionQuery</a>.</li>
<li>Caches the collection data and returns.</li>
</ol>
Function Discovery network providers only return function instances through the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface.  They return no function instances directly when this method is invoked. Instead, <a href="https://msdn.microsoft.com/library/windows/hardware/ff543208">Execute</a> simply initiates an entirely asynchronous retrieval operation and returns <b>E_PENDING</b> to indicate that the results will be returned asynchronously.   Notifications must be used to retrieve function instances from Function Discovery network providers.




## -see-also




<a href="https://msdn.microsoft.com/3c255fb4-8f9d-47a2-9770-1aa528d07f43">Function Discovery Queries</a>



<a href="https://msdn.microsoft.com/ae279ac1-ed7a-431b-a5aa-d60f5f9a64b0">IFunctionInstanceCollectionQuery</a>
 

 

